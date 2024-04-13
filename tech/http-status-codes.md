Discover a comprehensive **HTTP Status Code Cheat Sheet** detailing [official](#official-http-status-codes) and [unofficial status codes](#unofficial-http-status-codes) with clear descriptions and usage contexts. Perfect for developers and IT professionals seeking quick references and insights into both commonly used and obscure HTTP responses. Stay informed and efficient with this essential guide to understanding server-client interactions.

## Official HTTP Status Codes
### Status code Ranges
| Code | Description                                             |
|------|---------------------------------------------------------|
| [1xx](#1xx-informational-response)  | *Informational response* – the request was received, continuing process |
| [2xx](#2xx-success)  | *Successful* – the request was successfully received, understood, and accepted |
| [3xx](#3xx-redirection)  | *Redirection* – further action needs to be taken in order to complete the request |
| [4xx](#4xx-client-errors-21)  | *Client error* – the request contains bad syntax or cannot be fulfilled |
| [5xx](#5xx-server-errors)  | *Server error* – the server failed to fulfil an apparently valid request |
[More information](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes)

### 1xx Informational Response

| Code | Description                                         |
|------|-----------------------------------------------------|
| 100  | Continue                                            |
| 101  | Switching Protocols                                 |
| 102  | Processing (WebDAV; RFC 2518)                       |
| 103  | Early Hints (RFC 8297)                              |

### 2xx Success

| Code | Description                                                   |
|------|---------------------------------------------------------------|
| 200  | OK                                                            |
| 201  | Created                                                       |
| 202  | Accepted                                                      |
| 203  | Non-Authoritative Information (since HTTP/1.1)                |
| 204  | No Content                                                    |
| 205  | Reset Content                                                 |
| 206  | Partial Content                                               |
| 207  | Multi-Status (WebDAV; RFC 4918)                               |
| 208  | Already Reported (WebDAV; RFC 5842)                           |
| 226  | IM Used (RFC 3229)                                            |

### 3xx Redirection

| Code | Description                                             |
|------|---------------------------------------------------------|
| 300  | Multiple Choices                                        |
| 301  | Moved Permanently                                       |
| 302  | Found (Previously "Moved temporarily")                  |
| 303  | See Other (since HTTP/1.1)                              |
| 304  | Not Modified                                            |
| 305  | Use Proxy (since HTTP/1.1)                              |
| 306  | Switch Proxy                                            |
| 307  | Temporary Redirect (since HTTP/1.1)                     |
| 308  | Permanent Redirect                                      |

### 4xx Client Errors 2/1

| Code | Description                                                |
|------|------------------------------------------------------------|
| 400  | Bad Request                                                |
| 401  | Unauthorized                                               |
| 402  | Payment Required                                           |
| 403  | Forbidden                                                  |
| 404  | Not Found                                                  |
| 405  | Method Not Allowed                                         |
| 406  | Not Acceptable                                             |
| 407  | Proxy Authentication Required                              |
| 408  | Request Timeout                                            |
| 409  | Conflict                                                   |
| 410  | Gone                                                       |
| 411  | Length Required                                            |
| 412  | Precondition Failed                                        |
| 413  | Payload Too Large                                          |


### 4xx Client Errors 2/2

| Code | Description                                                |
|------|------------------------------------------------------------|
| 414  | URI Too Long                                               |
| 415  | Unsupported Media Type                                     |
| 416  | Range Not Satisfiable                                      |
| 417  | Expectation Failed                                         |
| 418  | I'm a teapot (RFC 2324, RFC 7168)                          |
| 421  | Misdirected Request                                        |
| 422  | Unprocessable Content                                      |
| 423  | Locked (WebDAV; RFC 4918)                                  |
| 424  | Failed Dependency (WebDAV; RFC 4918)                       |
| 425  | Too Early (RFC 8470)                                       |
| 426  | Upgrade Required                                           |
| 428  | Precondition Required (RFC 6585)                           |
| 429  | Too Many Requests (RFC 6585)                               |
| 431  | Request Header Fields Too Large (RFC 6585)                 |
| 451  | Unavailable For Legal Reasons (RFC 7725)                   |

### 5xx Server Errors

| Code | Description                                                   |
|------|---------------------------------------------------------------|
| 500  | Internal Server Error                                         |
| 501  | Not Implemented                                               |
| 502  | Bad Gateway                                                   |
| 503  | Service Unavailable                                           |
| 504  | Gateway Timeout                                               |
| 505  | HTTP Version Not Supported                                    |
| 506  | Variant Also Negotiates (RFC 2295)                            |
| 507  | Insufficient Storage (WebDAV; RFC 4918)                       |
| 508  | Loop Detected (WebDAV; RFC 5842)                              |
| 510  | Not Extended (RFC 2774)                                       |
| 511  | Network Authentication Required (RFC 6585)                    |



## Unofficial HTTP Status Codes
### Not Specified by Any Standard

| Code | Description                       |
|------|-----------------------------------|
| 218  | This is fine (Apache HTTP Server)|
| 419  | Page Expired (Laravel Framework) |
| 420  | Method Failure (Spring Framework)|
| 420  | Enhance Your Calm (Twitter)       |
| 430  | Request Header Fields Too Large (Shopify) |
| 430  | Shopify Security Rejection (Shopify) |
| 450  | Blocked by Windows Parental Controls (Microsoft) |
| 498  | Invalid Token (Esri)              |
| 499  | Token Required (Esri)             |
| 509  | Bandwidth Limit Exceeded (Apache Web Server/cPanel) |
| 529  | Site is overloaded                |
| 530  | Site is frozen                    |
| 530  | Origin DNS Error (Shopify)        |
| 540  | Temporarily Disabled (Shopify)    |
| 598  | Network read timeout error (Informal convention) |
| 599  | Network Connect Timeout Error     |
| 783  | Unexpected Token (Shopify)        |

### Cloudflare

| Code | Description                                    |
|------|------------------------------------------------|
| 520  | Web Server Returned an Unknown Error           |
| 521  | Web Server Is Down                             |
| 522  | Connection Timed Out                           |
| 523  | Origin Is Unreachable                          |
| 524  | A Timeout Occurred                             |
| 525  | SSL Handshake Failed                           |
| 526  | Invalid SSL Certificate                        |
| 527  | Railgun Error (obsolete)                       |
| 530  | Error 530 is returned along with a 1xxx error. |

### AWS Elastic Load Balancing

| Code | Description                                        |
|------|----------------------------------------------------|
| 000  | Returned with an HTTP/2 GOAWAY frame if the compressed length of any of the headers exceeds 8K bytes or if more than 10K requests are served through one connection. |
| 460  | Client closed the connection with the load balancer before the idle timeout period elapsed. Typically, when client timeout is sooner than the Elastic Load Balancer's timeout. |
| 463  | The load balancer received an X-Forwarded-For request header with more than 30 IP addresses. |
| 464  | Incompatible protocol versions between Client and Origin server. |
| 561  | Unauthorized (An error around authentication returned by a server registered with a load balancer. A listener rule is configured to authenticate users, but the identity provider (IdP) returned an error code when authenticating the user.) |

### nginx

| Code | Description                             |
|------|-----------------------------------------|
| 444  | No Response                             |
| 494  | Request header too large                |
| 495  | SSL Certificate Error                   |
| 496  | SSL Certificate Required                |
| 497  | HTTP Request Sent to HTTPS Port         |
| 499  | Client Closed Request                   |


### Microsoft IIS

| Code | Description              |
|------|--------------------------|
| 440  | Login Time-out           |
| 449  | Retry With               |
| 451  | Redirect (Exchange ActiveSync) |
