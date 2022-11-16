# Domain Name System (DNS)

The Domain Name System (DNS) is a network of servers, systems, and services that collaborate to resolve qualified domain names or URLs (such as .com, .net, .org, etc addresses) into addresses routable over the internet, most commonly IP addresses.

The basic DNS service operates over standard port 53 using UDP.

By default, the basic DNS service does not provide an encrypted connection, nor record validation (no confidentiality or integrity).

DNS can also operate over TLS and HTTPS for DNS servers that support the protocols to provide encrypted connections (confidentiality).

An additional service, DNSSEC, can provide record authentication (integrity); DNSSEC alone does not provide confidentiality.

When an application wishes to connect to a location on the internet, rather than specifying an IP address it can use the Domain Name System to convert a domain name to an IP address.

A benefit of this arrangement also allows endpoints to change endpoints locations (and IP addresses) without needing to specifically notify remote applications.

Domain names are heirarchical with a Fully Qualified Domain Name being arranged with the top level at the end. For example: in www.example.com., .com. is the top level domain, .example.com. is a domain name and www.example.com. is a sub-domain.

A fully qualified domain name will end in a . as the . indicates the root domain.

## DNS Requests

### Recursive Request

In order to resolve a domain to an IP address the following occurs:
1. A DNS request is made to a recursive resolver
1. The resolver queries the root domain server (.)
1. The root domain server answers with a top level domain server
1. The recursive resolver queries a top level domain server (e.g. .com)
1. The top level server returns the domain server (e.g. example.com)
1. The recursive resolver queries the domain server
1. The IP address to the requested domain is returned to the resolver

At this point the DNS resolver can return the IP address to the initial requester - this process is typically transparent to the requester.

### Iterative Request

With an iterative request, the DNS server receiving the request responds immediatelly with its best answer, without recursing to any other authoritative servers.

If the server doesn't have an entry, it will refer the requester to a lower level authoritative server.

### Non-recursive Request

WIth this request, the request is made to a server that already has the record, either because it is an authoritative server for that entry, or because the entry is cached.

## DNS Servers

### Recursive DNS Server (Recursor) (and DNS Resolver)

The Recursive DNS server recieves a DNS request and is responsible for making the subsequent DNS requests to other DNS servers at various levels until it finds a server that can return an authoritative answer for the DNS request.

The Recursive DNS server is often the first line DNS server that is accessed by a local application; this first line DNS server is most often referred to as the DNS resolver. It may be running on a Wireless Router or other internet gateway or at an ISP.

A Recursive DNS will often cache authoritative responses to speed up subsequent DNS requests.

### Authoritative DNS Server

The authoratative DNS server is the server that actually contains the domain records. It is typically at the bottom of the DNS chain and will be the last response recieved by a resolver before the IP address can be returned to the requester.

### Root DNS Server

A DNS server that can point a recursive request to a top level domain server (a .com, .org, .net server e.g.)

### Top Level DNS Server

A DNS server that represents a top level domain (such as .com, .org, .net) and can point to a recursive request to a domain server (typically to an authoritative server).

## Records

There are many kinds of records that DNS supports, which can and have been periodically expanded over the years.

Records act, superficially, as key-value rows, where each row has a type and a key, the combination of type and key specifies the value to be returned.

### A Type

The A record specifies the IPv4 address for a fully qualified domain name (FQDN).

For the A record, the FQDN is the key, specified in the request, and the IP address is the value, returned in the response.

### AAAA Type

The AAAA record specifies the IPv6 address for a FQDN.

It functions the same as an A type record, except it returns an IPv6 records.

### PTR Type

A PTR record is the reverse of an A type record, returning a domain name given an IP address.

The key is an IP address, and the response is a FQDN.

### CNAME

A CNAME record, or Canonical Name record, direct alias, or alternative, domain names to point to the canonical FQDN.

This is very often used for sub-domains that are hosted on a common IP addresses with the canonical domain.

In this arrangement the alias points to the canonical domain name, and then then the canonical domain A record is resolved for the IP address. With this, a change in IP address only has to be updated for a single record, rather than for all aliases.

Multiple CNAMEs can be present.

### MX

An MX record specifies the address for the domain's mail server.

Typically an MX record will specify a subdomain, or another CNAME record, which is then referenced to resolve the mail server IP.

Multiple MX records can be present.

### TXT

A TXT record is a record that allows for generic text input.

A TXT record can be used to record publically available administrative data related to the domain name.

### Wildcard 

Wildcard records can be used to capture all requests for all subdomains. This is useful if all subdomains of a domain will be hosted on a common IP.

This can be useful to specify a common record that would otherwise be shared across multiple subdomains, such as an MX record that points to a common CNAME regardless of subdomain.

For example, an MX record for *.example.com. would mean that all domains under example.com would be directed to the same MX.

## References

[1] https://www.cloudflare.com/learning/dns/what-is-dns/

[2] https://en.wikipedia.org/wiki/Domain_Name_System#DNSCrypt