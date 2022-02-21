# WebDevSECtool
Web security tools for security headers

### Webdevsec Developer Tools and cmd line

The following activities are useful in getting to know the browser's tools to examine HTTP requests and responses, in particular the security headers.
Inspect any website sources from chrome:

Request Headers:

**Upgrade-insecure-requests** header: This is the brower's way of requesting that the HTTP server uses HTTPS to communicate.

Response Headers:

Notable take aways to recognize are the date, status and `strict-origin-when-cross-origin`. `strict-origin-when-cross-origin` is when a link on an external website leads to the current link. This is usually logged for statistical analysis, such as ad payment. It also prevents your browser from sending information between https:// to http:// (secure HTTPS to plaintext HTTP)

**Strict-transport-security** tells an HTTP client that it should only be accessed over HTTPS and not HTTP

**X-xss-protection** this header detects if a cross-site script is being loaded, stop loading the page. Essentially another level of protection in case the page has been compromised
