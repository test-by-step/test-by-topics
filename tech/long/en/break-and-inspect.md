# Break and Inspect

Break and Inspect is the process of decrypting network traffic in order to inspect the contents.

Break and inspect functional involves network traffic decryption / deep packet inspection.

Break and Inspect is most often associated with data loss prevention and data loss detection.

Break and Inspect will typically occur on a forward proxy.

Most often, break and inspect requires endpoint devices to be installed with a special, organization internal trusted TLS certificate.

When a device connects to an HTTPS connection, the forward proxy establishes a connection to the server on behalf of the requesting endpoint. The connection is then decrypted at the forward proxy, inspected, and response to the original requesting device is returned but encrypted with the TLS certificate of the organization.

Break and Inpsect can inspect connections to external services for the upload of protected data.

Break and inspect may also be able to detect malware ingressing the system over an encrypted connection.