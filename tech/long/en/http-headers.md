# Proper Hypertext Transfer Protocol (HTTP) headers

## X-Frame-Options

> X-Frame-Options: DENY

Prevents page from loading iframe, frame, embed, object tags.

## X-XSS-Protection

> X-XSS-Protection: 0

Turn off this feature - this feature would stop a page from loading if it detected a XSS attack.

Content Security Policy in modern browsers are best suited for protecting against XSS.

## X-Content-Type-Options

> X-Content-Type-Options: nosniff

Turn off content type sniffing to ensure a browser does not mistakenly turn a content type into executable content when it should not be using MIME sniffing.

## Referrer-Policy

> Referrer-Policy: strict-origin-when-cross-origin

Restricts the information on the context of the originating site that is sent to a new page when linked from another page.

## Content-Type

> Content-Type: text/html; charset=UTF-8

Explicitly specify the character encoding of the page and the proper MIME type for the page.

## Set-Cookie

Use Set-Cookie to register a cookie value with the browser.

Set-Cookie using the HTTP cookie headers make the cookie inaccessible to scripts inline to the page (and resistant to XSS attacks).

## Strict-Transport-Security

Called HSTS. HTTP Strict Transport Security.

> Strict-Transport-Security: max-age=63072000; includeSubDomains; preload

Only allows HTTPS access to the domain and subdomains.

## Content-Security-Policy

Content Security Policy (CSP) is complex and application dependent.

A good CSP hardens an application against cross site scripting (XSS) attacks.

CSP can control what resources are allowed or available to load externally, and from where.

CSP can help to mitigate malicous externally linked scripts from being loaded onto the page but **does not** mitigate against insecure development practices that leave XSS vulnerabilities in the application itself.

## Access-Control-Allow-Origin

> Access-Control-Allow-Origin: https://yoursite.com

Explicitly allows external origins to access the resource - e.g. across different origins.

This can prevent malicious scripts from loading the resource from an unsafe domain, or from loading into an unsafe domain.

Part of Cross Origin Resource Sharing (CORS). CORS resources should explicitly list which domains are allowed to access them (rather than *).

## Cross-Origin-Opener-Policy

> HTTP Cross-Origin-Opener-Policy: same-origin

Isolates the browsing context exclusively to same-origin documents.

## Cross-Origin-Resource-Policy

> Cross-Origin-Resource-Policy: same-site

Limit current resource loading to the site and sub-domains only.

## Cross-Origin-Embedder-Policy

> Cross-Origin-Embedder-Policy: require-corp

## References

[1] https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Headers_Cheat_Sheet.html

[2] https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html