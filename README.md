# HTTP Status Codes

# What are HTTP status codes?

HTTP status codes are three-digit responses from the server to the browser-side request. Everyone has probably gotten the classic 404 page-not-found error. That is an HTTP client error status code and there are a lot more of them.

These status codes (also called response status codes) serve as a means of communication between the server and the internet browser and there are multiple code classes based on the type of information they are communicating. The differences in classes are indicated through the first digit of the error code, for example: just like a 404, any other 4xx will mean that in some way the page or website could not be reached, while a 2xx means that your request was successfully completed.


# How are HTTP status codes categorized?

HTTP status codes are split into 5 different categories. Each category will give you hints as to what the response was, even if you don't know the specific response code.

For an explanation of each category - and each individual status code - click on the corresponding link below or go to our complete list of HTTP status codes.

1xx - Informational: The server has received the request and is continuing the process 

2xx - Successful: The request was successful and the browser has received the expected information 

3xx (Redirection): You have been redirected and the completion of the request requires further action

4xx (Client Error): The website or the page could not be reached, either the page is unavailable or the request contains bad syntax 

5xx (Server Error): While the request appears to be valid, the server could not complete the request


# 1XX Status Codes

A 1XX-level status code tells you that the request you’ve made to the server is still in progress for some reason. This isn’t necessarily a problem, it’s just extra information to let you know what’s going on.

A 1xx Informational status code means that the server has received the request and is continuing the process. A 1xx status code is purely temporary and is given while the request processing continues. For most tasks you won't encounter these much, as it's not the final response to the request.


### HTTP Status Code 100: “Continue.”

This means that the server in question has received your browser’s request headers, and is now ready for the request body to be sent as well. This makes the request process more efficient since it prevents the browser from sending a body request even though the headers have been rejected.

100 Continue, this response means everything is functioning properly and can proceed. The code indicates the server is processing the request and can complete it. The 100 code is an interim response and tells you the request has not caused an error.


### HTTP Status Code 101: “Switching protocols.”

Your browser has asked the server to change protocols, and the server has complied.

101 Switching Protocol, the server received the data request and can comply. The server, however,
will change protocols based on information in the Upgrade header field. This status code does not
indicate an error.


### HTTP Status Code 102: "Processing".

The 102 Processing status code means that the server has accepted the full request but has not yet completed it and no response is available as of  yet.
An interim response used to inform the client that the server has accepted the complete request but has not yet completed it.

102 Processing, the server received the request, but there isn't any response yet. The server is
processing the request, which is ongoing. This code also indicates an error has not occurred.


### HTTP Status Code 103: “Early hints.”

This returns some response headers before the rest of the server’s response is ready.
The 103 Early hints status code is intended to be used to allow the user agent to preload resources, while the server prepares a response. It is intended to be primarily used with the Link Header.


### Reference

https://www.youtube.com/watch?v=_B93xM5TPuI&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=1
      
        
        
# 2XX Status Codes

A 2xx Succesful status code means that the request was successful and the browser has received the expected information. This is generally the one you want to see, as it means that the request was a success and has been received, understood and accepted it. As a website owner you should make sure that all pages and resources (images, videos, etc.) all return a 2xx status code. This means that browsers can reach it successfully and that your website visitors can see and use your website.


### HTTP Status Code 200: "Everything is OK.".

The 200 OK status code means that the request was successful, but the meaning of success depends on the request method used


### HTTP Status Code 201: "Created". 

A 201 Created status code is like a 200 OK status code, however, a 201 status code means that a request was successfully processed, and it returned, or created, a resource or resources in the process. A 201 status code is typically used for PUT requests. For example, when a PUT request is used, a new resource is created on the URL specified in the request. If there is a 201 status code in a POST request, it means a resource was created at a different API endpoint/location.


### HTTP Status Code 202: “Accepted”.

The 202 Accepted status code means that the server has received a request for processing, and it is been accepted, but the request has not been completed. It also does not mean the request will eventually be accepted, as it will depend on when the actual processing takes place. This type of request is typically seen in APIs where a batch process is run once a day. Since there is no way for HTTP to communicate after a request has succeeded or user’s connection has been closed, an API might send off an email to a user notifying them that the process has


### HTTP Status Code 203: “Non-Authoritative Information”. 

The 203 Non-Authoritative Information status code is typically used by an HTTP proxy or third party. The proxy, sitting between the client and server may change the responses before reaching the client. To indicate that something was changed during the process, a status code 203 is used. However, the drawback of this method is that it is not possible to know what the original status code was if a proxy changed something in the response. A suggested workaround is to use a warning header along with a 214 status code, which is used to indicate that there was a change or modification in the response. Using the warning header allows the original status code to passed through

203 Non-Authoritative Information, the returned data does not match the data available on the
server. This often can indicate the data arrived via a proxy source of the server that contained the
original data. This code means the server received a 200 OK from its origin, but it's returning a
modified version of the response.


### HTTP Status Code 204: “No Content”.

A status code of 204 indicates that the response has been successfully delivered by the server and fulfilled and no further content is to be sent in the body of the response. As an example, if the request is sent in the form on a page, once the response is sent, the client/browser is not supposed to change the view, meaning the form should not be refreshed or direct users to a new page. No additional content should be replaced or appear in terms of the user’s perspective

204 No Content, the server sends this code when it received and understood the request. With this
code, though, the server is signaling it has no data to return. Even though there's no content to send,
this code indicates the HTTP headers are proper.

### HTTP Status Code 205: “Reset Content”.

Like the 204 No Content status code, a status code 205 Reset Content indicates that the server has sent the request successfully and requires the user agent to refresh/reset the view to its original state. If we use the example of a form on a page, once the user completes and submits the form, the client/browser should clear the form back to its original state so a user can take further action. A 205 status code assumes no further content will be provided.

205 Reset Content, the server has completed the request, but there was a problem. This status code
represents a correctable error. You can solve this by resetting the document view and trying again.


### HTTP Status Code 206: “Partial Content”. 

A 206 Partial Content status code can be used for a variety of requests and typically indicates that the server has fulfilled a partial request for a resource. For example, if a client is only looking for a specific portion, or range, of a specific resource or page. Another example of where a 206 status code is used is in video. A client may only load video in pieces as to not have to wait for the video to buffer or load, helping to avoid a negative user experience where a user would have to wait longer before the video plays. This is normal best practice among HTTP video players to avoid bandwidth and perceived latency issues.


### Reference

https://www.youtube.com/watch?v=Q-0Rd-la7PQ&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=2


# 3XX: Redirection

  The 3xx status codes are used in cases of URL redirection. Websites are always changing and evolving, so there may be times where marketers need to direct users to an updated, or different page. Redirects help alleviate users from having to search for what they are looking for and maintain your ranking in search engines. The redirect actions may be carried out by the browser automatically or may require additional interaction from users. The 3xx HTTP status codes are vital for SEO (Search Engine Optimization) and user experience, as well as tell search engines what content you want them to crawl and index. If not properly implemented, users may be directed to an unintended location, which could result in a 4xx status code and could affect SEO quality scores.


### HTTP Status Code 300: “Multiple Choices.”

   Sometimes, there may be multiple possible resources the server can respond with to fulfill your browser’s request. A 300 status code means that your browser now needs to choose between them. This may occur when there are multiple file type extensions available, or if the server is experiencing word sense disambiguation.

  The 300 Multiple Choices status code indicates that a resource has moved and can redirect to multiple locations. In this case the user must decide which resource to use. The server may indicate a preferred choice and that should be indicated in the header field where the user agent could redirect to the preferred choice automatically. In practical use, this status code is rarely used as there is no standardized way to choose from multiple responses. See RFC7231, Section 6.4.1 for more information. 
  
300 Multiple choices, The request has more than one potential response. The server often sends a
report with this code that includes a list of the potential choices. To get the data, you can choose
from the responses the server provides.  

### HTTP Status Code 301: Moved Permanently

  “The requested resource has been moved permanently.” This code is delivered when a web page or resource has been permanently replaced with a different resource. It is used for permanent URL redirection.

   A 301 Moved Permanently status code is utilized to indicate that a target resource has been moved to a permanent location. The 301 status code tells the browser/client to use this new location or URL going forward in the header. Along with the 301 status code, the new URL will be given in the response as well as update any URLs in the previous location(s), along with updating to the new URL. See RFC7231, Section 6.4.2 for more information.
   
301 Moved permanently, This code indicates the URL no longer exists or is broken. This message
often includes the new URL for you to use. It also signifies to the user to update all references to this
URL.   


### HTTP Status Code 302: Found

  “The requested resource has moved, but was found.” This code is used to indicate that the requested resource was found, just not at the location where it was expected. It is used for temporary URL redirection.

  A 302 Found status code indicates to a client/browser that a resource that they are accessing is temporarily located under a different location. Unlike the 301 status code, a 302 status code indicates a temporary move, so the client should not automatically update its links to the new location, as again, it is meant to be temporary. An example of where the 302 status code should be used if there are multiple URLs, but they could be served in different languages. A user may arrive at specific URL, but the client may redirect them automatically to the proper page based on their browser settings and use this on subsequent visits. It is noted that in some cases, browsers may change a request from POST to GET. In the case that this action is not favorable, a 307 status code should be used. See RFC7231, Section 6.4.3 for more information.  

302 Found, The Uniform Resource Identifier (URI) changed, but the change is not permanent. A 302
Found means more changes might occur in the future, so consider using the new URI to complete
requests. This code is one way to create a temporary redirect.

### HTTP Status Code 303: See Other

  Understanding a 303 status code requires that you know the difference between the four primary HTTP request methods. Essentially, a 303 code tells your browser that it found the resource your browser requested via POST, PUT, or DELETE. However, to retrieve it using GET, you need to make the appropriate request to a different URL than the one you previously used.

  A status code 303 See Other indicates that a server will be redirecting the client/browser to another resource. The resource will be indicated as a URL the header field. Unlike the 301 and 302 status codes, it does not mean a resource has temporarily or permanently move, its intent is to specify the URL to where the response to the specific request can be found via a GET request. 303 status codes should not be cached, however, the response to the subsequent request may be cached. A typical use of the 303 status code would be to ensure users do not accidentally resubmit form data via a POST request. They should be directed to a new page. If not, they may unknowingly click the back button in their browser, which may ask them to resubmit again, which leads to unnecessary duplicate submissions. See RFC7231, Section 6.4.4 for more information.  


### HTTP Status Code 304: Not Modified

  “The requested resource has not been modified since the last time you accessed it.” This code tells the browser that the resources stored in the browser cache haven’t changed. It’s used to speed up web page delivery by reusing previously-downloaded resources.

  A status code of 304 Not Modified is sent in response to a conditional GET or HEAD request. Clients/browsers can send a conditional request, such as If-Match, If-None-Match, If-Modified-Since, If-Unmodified-Since, or If-Range, asking if a specific resource has been modified since a specific date/time. This is done only if the client has previously accessed, downloaded, and saved the resource. If it has been modified since that specific date/time last accessed, the server will return a 200 OK status code. If it has not been changed since that date/time, the 304 status code is sent as the response, indicating that the saved resource should be served since it has not been modified since the last time it was accessed. See RFC7232, Section 4.1 for more information.         


### HTTP Status Code 305: Use Proxy

  The 305 Use Proxy status code is a deprecated status code that is no longer used due to security consideration. It was used to indicate to a client that the resource they were accessing must be accessed via a proxy. For more information on the 305 Use Proxy status code, see RFC7231, Section 6.4.5         

305 Use proxy, The request needs to use a server proxy to complete successfully. This message tells
the user to send the request again. The second request will go to the server proxy, which can
provide the data.

### HTTP Status Code 306: Unused

  Like the 305 status code, the 306 Unused status was originally known as Switch Proxy. The 306 status code was used in a previous specification. Its intention was to be used as in indication to the client that subsequent requests to a resource should use the proxy that was specified. This was deemed as a security issue, so it is no longer used. For more information on the 306 Unused status code, see RFC7231, Section 6.4.6        


### HTTP Status Code 307: “Temporary Redirect.”

  This status code has replaced 302 “Found” as the appropriate action when a resource has been temporarily moved to a different URL. Unlike the 302 status code, it does not allow the HTTP method to change.

  Like the 302 Found redirect status code, the 307 Temporary Redirect status code indicates to the client/browser that a resource or document is available at a different, temporary URL and returns that URL. Since the redirection is temporary and could change, the browser/client should continue to access the current URL for subsequent requests. The main difference between the 302 status code and the 307 status code is that the 307 status code does not allow changing requests from a POST request to a GET request, so if the client requested POST request, it be redirected and initiate the POST request again. See RFC7231, Section 6.4.7          

307 Temporary redirect, This response means the Uniform Resource Identifier is different. The
server has to use a new, temporary URI to return data. This code also indicates future requests
likely won't use the temporary URI and will function as normal.

### HTTP Status Code 308: “Permanent Redirect.”

  The 308 status code is the successor to the 301 “Moved Permanently” code. It does not allow the HTTP method to change and indicates that the requested resource is now permanently located at a new URL.

  A 308 Permanent Redirect status code is a cacheable status code (unless cache controls are implemented) that indicates that a target resource is now located at a permanent URL and subsequent requests should be directed to that URL as well. Additionally, the client should update any old bookmarks to the new location. The 308 status code is very similar to the 301 status code, however, if a 308 status code is sent, the client has to initiate and send the same request on the target location. A 301 status code does not have to do this. Most browsers/clients change the POST request to a GET request. See RFC7238, Section 3 for more information.         


### Reference    

https://www.youtube.com/watch?v=cGXRK6xVUGw&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=11

        
        
# 4XX : Client Error

A 4xx Client Error status code means that the website or the page could not be reached and either the page is unavailable or the request contains bad syntax. As a website owner you should do your best to avoid these, as it means your users will not find what they're looking for. This can be either pages that are no longer found and are either temporarily or permanently gone. Besides giving a bad user experience, it can also hurt your SEO efforts.


### HTTP Status 400 : “Bad Request.” 

The server can’t return a response due to an error on the client’s end. See our guide for resolving this error.
The 400 Bad Request status code means that the server could not understand the request because of invalid syntax.

A 400 Bad Request error status code means that the server cannot process the request due to an issue from the client. This could be due to any number of reasons, such as a file being too large, bad syntax, an invalid URL, or some other issue caused by a third-party application, which is why the 400 status code is sometimes uses as a catch all status code, even if there is an issue on the server-side. This can make troubleshooting a 400 status code a bit more time consuming and difficult, however, along with the 400 status code error and header information, the server can provide additional response along with it, which can be displayed to the user to help identify the issue and ease the process of troubleshooting and diagnosing the error. See RFC7231, Section 6.5.1 for more information. 

400 Bad request, this code indicates invalid syntax prevented the server from receiving a request.
Servers return this code when the requester made the error and should correct it before trying
again. This could mean the client used invalid message framing or improperly routed the message.

### HTTP Status 401 : “Unauthorized” or “Authorization Required.” 

This is returned by the server when the target resource lacks valid authentication credentials. You might see this if you’ve set up basic HTTP authentication using htpasswd.

The 401 Unauthorized status code means that the request has not been applied because the server requires user authentication.

A 401 Unauthorized error status code indicates that the request does not include the appropriate authentication credentials, authentication has failed, or the user must log in. The client requires authentication from the server. The terms authorized and authenticated are often use interchangeably, but they mean separate things. A status code of 401 is strictly concerned with authentication. In cases where you would want to inform a client that they are not allowed at all, then a status code of 403 should be implemented. According to the specification, the 401 status code must also include the WWW-Authenticate header from the server response, indicating to the client what authentication scheme or method the server requires. See RFC7235, Section 3.1 for more information.  

401 Unauthorized, the server cannot complete the request. The server believes the user does not
have the authorization to receive the data. After sending this code, a server won't complete the
request until user authentication happens.

### HTTP Status 402 : “Payment Required.” 

Originally, this code was created for use as part of a digital cash system. However, that plan never followed through. Instead, it’s used by a variety of platforms to indicate that a request cannot be fulfilled, usually due to a lack of required funds. Common instances include:
You’ve reached your daily request limit to the Google Developers API.
You haven’t paid your Shopify fees and your store has been temporarily deactivated.
Your payment via Stripe has failed, or Stripe is trying to prevent a fraudulent payment.

The 402 Payment Required status code is a response reserved for future use. It was originally created to be implemented in digital payment systems, however, it is rarely used and a standard convention of using it does not exist.

Originally created as part of a way to allow for potential future digital payment methods, the 402 Payment Required error status code is officially reserved for future use, but it used some limited, but rare, situations. For more information on the 402 Payment Required error code, see RFC7231, Section 6.5.2   


### HTTP Status 403 : “Access to that resource is forbidden.” 

This code is returned when a user attempts to access something that they don’t have permission to view. For example, trying to reach password-protected content without logging in might produce a 403 error.

The 403 Forbidden status code means that the client request has been rejected because the client does not have rights to access the content. Unlike a 401 error, the client's identity is known to the server, but since they are not authorized to view the content, giving the proper response is rejected by the server.

The 403 Forbidden error status code indicates that the request from the client was understood, but the server will not authorize it, so the client cannot access it. The server can make known the reason it will not authorize the request within the response, which could be due to various reasons like incorrect password or username. Unlike the 401 status code, which require authentication, a 403 status code can indicate that the client truly does not have authorization to access those resources, so authentication in this instance is not possible. See RFC7231, Section 6.5.3 for more information. 

403 Forbidden, the server understood the request, but it is refusing to fulfill it. Sometimes, the user
does not have access to the requested content or data, and the server rejects the request. This also
can mean the client needs an account to request data or the request would create a duplicate record.

### HTTP Status 404 : “The requested resource was not found.” 

This is the most common error message of them all. This code means that the requested resource does not exist, and the server does not know if it ever existed.

The 404 Not Found status code means that the server either did not find a current representation for the requested resource or is trying to hide its existence from an unauthorized client.

When looking at things SEO-wise the 404 Not Found status code pages with a high volume of traffic should be redirected using a 301 to the most relevant page possible. For some pages, however, a 404 might be necessary, for example, if the product is out of stock for an extended period of time. If you have external links pointing to a page that returns 404, you will lose the link equity those links would otherwise give.

One of the most common and infamous status codes encountered by users and developers, the 404 Not Found error status code indicates that the resource required from the server does not exist or is not willing to provide it to the client. A 404 status code will not indicate whether the lack of providing the resource is temporarily or permanently, but the client can make subsequent requests to access it. In cases where its known that the resources are permanently gone, the 410 status code should be used. 404 status codes, by default, are also cacheable, unless other cache controls are in place. See RFC7231, Section 6.5.4 for more information. 

404 Not found, the 404 error is one of the most common codes servers send. The error means the
server can't find information in that location now, but it might be able to in the future. It also can
occur when a page has a new location, but a user didn't provide the old one with a redirect.

### HTTP Status 405 : “Method not allowed.” 

This is generated when the hosting server (origin server) supports the method received, but the target resource doesn’t.

The 405 Method Not Allowed status code means that while the server knows the request method, the method has been disabled and can not be used.

The 405 Method Not Allowed error status code indicates that a specific resource requested by the client is not supported by the server. The 405 Method Not Allowed is like the 403 Forbidden status code, however, the 403 status code indicates that the resource may be available, it is just that the client does not have the necessary authorization to carry out the request. Along with the 405 Method Not Allowed status, the server must indicate the appropriate and supported methods for the target resource. For more information on the 405 Method Not Allowed error code, see RFC7231, Section 6.5.5  


### HTTP Status 406 : “Not acceptable response.” 

The requested resource is capable of generating only content that is not acceptable according to the accept headers sent in the request.

The 406 Not Acceptable status code is sent by the server when it does not find any content following the criteria given by the user agent.

Like the 405 Method Not Allowed error status code, the 406 Not Acceptable error code indicates that there is not support for a specific request. In this case the 406 Not Acceptable status code indicates that the server understood the request, but the response is not supported or understood by the client. A client can request specific versions of a resource in the header, such as A-IM or Accept Language, among others, but if the server does not support it, it responds with the 406 Not Acceptable status code. The server can either respond with a list of appropriate resource identifiers that the client can choose from. See RFC7231, Section 6.5.6 for more information.  


### HTTP Status 407 : “Proxy Authentication Required.” 

A proxy server is in use and requires your browser to authenticate itself before continuing.

The 407 Proxy Authentication Required status code means that the client must first be authenticated by a proxy (similar to a 401).

The 407 Proxy Authentication Required error status code is like the 401 Unauthorized status code, however, in the case of a 407 status code, in order to use a proxy, the client must first be authenticated. The proxy must return the method for authentication. Not as common today due to the rise of VPNs, proxies act as intermediaries between users/clients and the Internet, allowing users to access resources more quickly, as content is typically cached, and can also provide a layer of security and anonymity for users. For more information on the 407 Proxy Authentication Required error code, see RFC7235, Section 3.2  


### HTTP Status 408 : “The server timed out waiting for the rest of the request from the browser.” 

This code is generated when a server times out while waiting for the complete request from the browser. In other words, the server didn’t get the full request that was sent by the browser. One possible cause could be net congestion resulting in the loss of data packets between the browser and the server.

The 408 Request Timeout status code means that the server did not receive a complete request in the time that it prepared to wait.

A 408 Request Timeout error status code means that the server did not receive a request from the client in a specified amount of time. A delayed request from the client can be due for a variety of reasons, such as a slow or broken connection. Once that time has passed, the 408 Request Timeout status is sent by the server and the user/client can resend the request again. For more information on the 408 Request Timeout error code, see RFC7231, Section 6.5.7 

408 Request timeout, this code means a request took too long to process. It also could indicate the
request didn't make it through to the server. Sometimes, internet problems can interrupt the
process, but the user can try again.

### HTTP Status 409 : “Conflict.” 

A 409 status code means that the server couldn’t process your browser’s request because there’s a conflict with the relevant resource. This sometimes occurs due to multiple simultaneous edits.

The 409 Conflict status code means that the request could not be fulfilled due to a conflict with the current state of the target resource and is used in situations where the user might be able to resubmit the request after resolving the conflict.

A 409 Conflict error status code indicates that the request from the client could not be processed due to a conflict with the server. The request from the client was fine, but there were issues on the server-side that prevents the request from being executed. An example of this could be if there was a request for a specific file to be edited, deleted, or created by the user, but those functionalities are not allowed. Along with the 409 response, the server should return instructions on how the user can resolve this issue or indicate why the issue is occurring. See RFC7231, Section 6.5.8 for more information. 



### HTTP Status 410 : “The requested resource is gone and won’t be coming back.” 

This is similar to a 404 “Not Found” code, except a 410 indicates that the condition is expected and permanent.

The 410 Gone status code means that the target resource has been deleted and the condition seems to be permanent. 

When looking at things SEO-wise the 410 Gone status code is a more permanent version a 404. The page will no longer be available from the server and has no forwarding address available. If you want to completely remove a page from Googles search index, then using 410 on a page is the proper way of doing it (instead of simply 404). 

Like the 404 Not Found error status code we covered earlier, the 410 Gone status code indicates that the resource the client is requesting has been removed and no longer available from the server. No further information is provided in terms of URL redirection or where to access the resource. It has been removed indefinitely. For more information on the 410 Gone error code, see RFC7231, Section 6.5.9  

410 Gone, the information a user requested from the server no longer exists. This code means the
information existed at some point, but it doesn't anymore. The server also can't tell you whether the
information exists somewhere else.

### HTTP Status 411 : “Length Required.” 

This means that the requested resource requires that the client specify a certain length and that it did not.

The 411 Length Required status code means that the server has rejected the request because it requires the Content-Length header field to be defined.

The 411 Length Required error status code indicates that the server does not allow the request from the client due to a predefined request body content length. The request can be repeated by the client if a valid Content-Length header is specified in the subsequent resource request. For more information on the 411 Length Required error code, see RFC7231, Section 6.5.10  


### HTTP Status 412 : “Precondition Failed.” 

Your browser included certain conditions in its request headers, and the server did not meet those specifications.

The 412 Precondition Failed status code means the server does not meet one or multiple preconditions that were indicated in the request header fields.

Conditional requests to the server are allowed as part of the HTTP protocol. If the right conditions are met in the request, the request is executed and processed by the server. A 412 Precondition Failed error status code means that one, or several, conditions in the request header has failed. For example, this can be used in GET requests and a conditional request is utilized to return the resource only if that resource has changed. For more information on the 412 Precondition Failed error code, see RFC7232, Section 4.2  


### HTTP Status 413 : “Payload Too Large” or “Request Entity Too Large.” 

Your request is larger than the server is willing or able to process.

The 413 Payload Too Large status code means the server refuses to process the request because the request payload is larger than the server is able or willing to process. While the server may close the connection to prevent the client from continuing the request, it should generate a Retry-After header field and after how long can the client retry.

The 413 Request Entity Too Large error status code indicates that the server will not accept and process the request due to the request body being larger than the server will allow or can process. Such examples include uploading a file where the file exceeds the maximum upload size set by the server or when the maximum number of uploads has been exceeded. In cases where the 413 Request Entity Too Large error occurs, the server may close the connection completely to prevent the client from continuing to sending the request. In some cases, it is likely the server would allow the client to retry the request, if itis a temporary condition, and should include that message back to the client. However, it is possible the request could cause the server itself to run out of physical disk space. In this case, the 507 Insufficient Storage error is the response that the client should receive back. See RFC7231, Section 6.5.11 for more information.  

### HTTP Status 414 : “URI Too Long.” 

This is usually the result of a GET request that has been encoded as a query string that is too large for the server to process.

The 414 URI Too Long status code means that the server is refusing to service the request because the request-target was longer than the server was willing to interpret.

Not a very common server response, the 414 URI Too Long error status code means that the server refused the client request due to the URL being longer than the server can process. Browsers and search engines do put limits on the length of URLs, partly to avoid DDoS attacks or code errors, but the path of a URL or HTTP does not have explicit limits. So, if limit exceeds what is set by the server, the 414 URI Too Long error will occur. For more information on the 414 URI Too Long error code, see RFC7231, Section 6.5.12  

### HTTP Status 415 : “Unsupported Media Type.” 

The request includes a media type that the server or resource doesn’t support.

The 415 Unsupported Media Type status code means that the server is rejecting the request because it does not support the media format of the requested data.

The 415 Unsupported Media Type error status code indicates the server cannot process the request body, or part of the request body, due to an unsupported media format. Even if the request from the client is supported, the 415 error may be returned if there is unsupported content in the body of the request. A 415 Unsupported Media Type error code is like the 406 Not Acceptable status code. The difference is that a 406 Not Acceptable error code is not due to the content in the header or encoding, rather, it is due to the value set within the HTTP header. Ensuring that the server can process the defined format along with sending the request with the correct form will avoid a 415 Unsupported Media Type error status code from happening. See RFC7231, Section 6.5.13 for more information. 

### HTTP Status 416 : “Range Not Satisfiable.” 

Your request was for a portion of a resource that the server is unable to return.

The 416 Range Not Satisfiable status code means that the range specified in the Range header field of the request can't be fulfilled. The reason might be that the given range is outside the size of the target URI's data.

As mentioned with the 206 Partial Request status code, it is possible for clients/browsers to request a partial response back from the server, whether it is a specific part of a file or video for example. Clients and servers use what is called range requests to execute these requests. However, if the server does not support these types of requests, it will simply return the entire resource along with a 200 OK response. If the server does support range requests, that is where the 416 Partial Request error status code enters the picture and will return what the client is asking for. In a situation where the server does support range requests, but the server does not agree with the request received because it does not fall within the range or possibly beyond the specified range, the 416 Range Not Satisfiable error status code will be returned. See RFC7233, Section 4.4 for more information.  

### HTTP Status 417 : “Expectation Failed.” 

The server is unable to meet the requirements specified in the request’s expect header field.

The 417 Expectation Failed status code means that the Expectation indicated by the Expect request-header field could not be met by the server.

Clients can use an Expect header to indicate that it expects specific behavior from the server. Like described in the 100 Continue status code, clients can check with the server if it will accept a request. If it does, the server will respond with the 100 Continue status code. If not, the 417 Expectation Failed error status code indicates that the server did not understand the Expect header or support it, therefore it cannot process the client request. For more information on the 417 Expectation Failed error code, see RFC7231, Section 6.5.14  

### HTTP Status 418 : “I’m a teapot.” 

This code is returned by teapots that receive requests to brew coffee. It’s also an April Fool’s Joke from 1998.

The 418 I'm a Teapot status code means that the server refuses to brew coffee because it is, in fact, a teapot. (It is a reference to a 1998 April Fools' joke called ''Hyper Text Coffee Pot Control Protocol'').

Error status codes 418-421 are currently unassigned, however, status code 418 I’m a Little Teapot is used in some instances. Created as an April Fool’s joke, it has gained some traction and is sometimes used as a joke or Easter egg and not used for actual everyday purposes. Most browsers ignore it as it is not an official status code. Another one in this category is the 420 Enhance Your Calm error status code that was introduced by Twitter. It is an error code that tells clients that they are being rate limited, which is a restriction on the number of requests they can make within a specified time period. Since 1989, the RFC Editor will publish the more humorous RFCs. Wikipedia has a full rundown of the more humorous April Fool’s RFCs. 


### Reference:

https://www.youtube.com/watch?v=mnqQ4y2JIC0&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=3

        
# 5xx: Server Error 

A 5xx Server error status code means that while the request appears to be valid, the server could not complete the request. If you're experiencing 5xx server errors for your website, you should immediately look at your server. If you're hosting your own server you'll need to start debugging to figure out why it is not responding properly. If you're using an external hosting provider you'll need to reach out to them, so they can look at it.


### HTTP Status Code 500: “There was an error on the server and the request could not be completed.” 

This is generic code that simply means “internal server error”. Something went wrong on the server and the requested resource was not delivered. This code is typically generated by third-party plugins, faulty PHP, or even the connection to the database breaking. Check out our tutorials on how to fix the error establishing a database connection and other ways to resolve a 500 internal server error.

The 500 Internal Server Error status code means that the server has encountered a situation that it does not know how to handle.
When looking at things SEO-wise the 500 Internal Server Error indicates a problem with the server, not the actual availability of the content. Since bots and users will both be lost, the link equity will go down fast.

The 500 Internal Server Error status code simply means that the server encountered an issue and cannot process the request. Typically, the 500 Internal Server Error code used more as a generic server error code if the exact issue does not fall within any of the other 5xx Server Error status code specifications. The 500 Internal Server Error code is probably the most used of the 5xx Server Error classification codes. See RFC7231, Section 6.6 for more information. 

500 Internal Server Error, a generic error message, is given when an unexpected condition was
encountered and no more specific messages are suitable.

### HTTP Status Code 501: Not Implemented

A 501 Not Implemented error status codes occurs when the server does not recognize the method of the request and therefore, cannot support or process the request. It is like the 405 Method Not Allowed client error status code, but a 501 Not Implemented error status code could indicate that the request method from the client is valid, just not supported by the server. The 405 Method Not Allowed error status would indicate that the method called by the client is not supported and should not have been utilized. See RFC7231, Section 6.6.2 for more information.  

The 501 Not Implemented response code means that the request can not be handled because it is not supported by the server.

501 Not Implemented, the server either does not recognize the request method or lacks the ability to
fulfill the request. Usually, this implies future availability (e.g., a new feature of a web-service API).

### HTTP Status Code 502: “Bad Gateway.” 

This error code typically means that one server has received an invalid response from another, such as when a proxy server is in use. Other times a query or request will take too long, and so it is canceled or killed by the server and the connection to the database breaks. 

The 502 Bad Gateway error status code means that a server is acting a proxy and it received a response from an origin server that came back as invalid. It is possible it is due to an overloaded server and the client can resubmit the request, but in most cases, it is due to an issue with the web server or CDN (Content Distribution Network) sitting between the client and server and may require additional troubleshooting with the hosting provider to understand why the error is being thrown. See RFC7231, Section 6.6.3 for more information.  

The 502 Bad Gateway response code means that the server received an invalid response while working as a gateway to handle the response.

502 Bad Gateway, the server was acting as a gateway or proxy and received an invalid response
from the upstream server.

### HTTP Status Code 503: “The server is unavailable to handle this request right now.” 

The request cannot be completed at this point in time. This code may be returned by an overloaded server that is unable to handle additional requests. We have a full guide on how to fix the 503 Service Unavailable Error.

The 503 Service Unavailable error status code indicates the server is currently overloaded with requests or out of resources, is currently in maintenance, or possibly that the application they are trying to access is down, and the server unable to complete the request due to the current state. Clients will sometimes see a message along with the 503 Service Unavailable error status code telling them to try the request again later. However, it may not provide a definitive explanation of when or how long the 503 Service Unavailable error status code may last. See RFC7231, Section 6.6.4 for information.  

The 503 Service Unavailable response code means that the server is currently not ready to handle the request. This is a common occurrence when the server is down for maintenance or is overloaded.

When looking at things SEO-wise the 503 Service Unavailable status code means that the server is unavailable and the visitor, bot or human, is asked to return again at a later time. This could be because of either server maintenance or server overload and search engines know to come back and check the availability later.

503 Service Unavailable, the server cannot handle the request (because it is overloaded or down for
maintenance). Generally, this is a temporary state

### HTTP Status Code 504: “The server, acting as a gateway, timed out waiting for another server to respond.” 

This is the code returned when there are two servers involved in processing a request, and the first server times out waiting for the second server to respond. You can read more about how to fix 504 errors in our dedicated guide.

Like the 502 Bad Gateway error status code, the 504 Gateway Timeout error status code is used when the server is acting as proxy but will respond with a 504 Gateway Timeout error status code if the response from an origin server takes too long to respond. A 502 Bad Gateway error status code should be used in cases where the response was invalid or not received by the proxy server at all. The message along with the 504 Gateway Timeout may indicate and recommend that the client try resending the request. See RFC7231, Section 6.6.5 for more information. 

The 504 Gateway Timeout response code means that the server acting as a gateway could not get a response time.

504 Gateway Timeout, the server was acting as a gateway or proxy and did not receive a timely
response from the upstream server

### HTTP Status Code 505: “HTTP Version Not Supported.” 

The server doesn’t support the HTTP version the client used to make the request.

A 505 HTTP Version Not Supported error status code means that the server does not support the version of the HTTP protocol used in the message of the request, and therefore, cannot process the request. Along with the 505 HTTP Version Not Supported error status code, the response from the server should include a message indicating why that specific HTTP protocol is not supported and which protocols are supported. See RFC7231, Section 6.6.6 for more information.  

The 505 HTTP Version Not Supported response code means that the version of HTTP used in the request is not supported by the server.

505 HTTP Version Not Supported, the server does not support the HTTP protocol version used in
the request.

### HTTP Status Code 506: Variant Also Negotiates

The 506 Variant Also Negotiates response code means that the server has the following internal configuration error: The chosen variant resource is configured to engage in transparent negotiation itself, therefore it cannot be a proper endpoint in the negotiation process.

The 506 Variant Also Negotiates is an experimental HTTP status code and is not part of the standard today. A 506 Variant Also Negotiates indicates that there in an internal configuration issue with the server due to content negotiation issues. Content negotiation allows clients to send multiple accept headers and tells the server which specific representation of a resource to serve as indicated by the browser. This could be for serving up the right language, document format, etc. Even though the 506 Variant Also Negotiates error status code is in an experimental status and not officially part of the HTTP standard, is used in rare cases. Some Google Play users encountered this issue in the past when trying to download multiple versions of an application, causing their devices to continually try to download the app in a closed loop process. See RFC2295, Section 8.1 for more information.  



### HTTP Status Code 507: Insufficient Storage
A 507 Insufficient Storage server error status code is also part of the WebDAV protocol. The 507 Insufficient Storage error status code indicates to the client that the request, such as a PUT or POST request, was too large in file size. It can also indicate that the server has temporarily run out of storage. See RFC4981, Section 11.5 for more information.  

The 507 Insufficient Storage status code means that the method could not be performed on the resource because the server is not able to store the representation that would be needed to complete the request successfully.



### HTTP Status Code 508: “Resource Limit Is Reached” limits on resources set by your web host have been reached. 

The 508 Loop Detected server error status code, like the 507 Insufficient Storage server error code, is part of the WebDAV protocol. Within the WebDAV protocol, it is possible the client can make a request to a server for an entire directory and create a target somewhere that same directory, resulting in an infinite request/response loop. The 508 Loop Detected server error status code indicates that the server ended the client request, specifically Depth: Infinity, because the server identified the request as resulting in an infinite loop, repeatedly calling back on itself. See RFC5842, section 7.2 for more information. 

The 508 Loop Detected response code means that the server has detected an infinite loop while processing the request.


### HTTP Status Code 509: “Bandwidth Limit Exceeded” means your website is using more bandwidth than your hosting provider allows.
The 509 server error status code is currently unassigned. 



### HTTP Status Code 510: Not Extended

A 510 Not Extended server error status code is currently in proposed/experimental status and not part of the standard HTTP status code specification. The 510 Not Extended indicates to the client that the request requires an extended HTTP request. If the server responds with the 510 Not Extended server error status code, it should also include how the client should remedy their request, but the specification does not explicitly state that. There’s debate whether this should fall under the 5xx server error classification since it could be viewed as a 4xx client error, but since it is not formally part of the standard, it is not relevant and rarely used for everyday use. See RFC2774, Section 7 for more information.  

The 510 Not Extended response code means that further extensions are required for the server to be able to fulfil the request.



### HTTP Status Code 511: “Network Authentication Required.” 

This status code is sent when the network you’re trying to use requires some form of authentication before sending your request to the server. For instance, you may need to agree to the Terms and Conditions of a public Wi-Fi hotspot.

The 511 Network Authorization Required server error status code that requires the client to authenticate itself in order to gain access to a network. For example, users might see this when trying to connect to a public Wi-Fi network at a business and users must agree to their terms and conditions before being granted access. Along with the 511 Network Authorization Required server error response, users should also be directed to where they can log in. See RFC6585, Section 6 for more information. 

The 511 Network Authentication Required response code indicates that the client needs to authenticate to gain network access. 


### Reference:

https://www.youtube.com/watch?v=wCMDwngoxUM&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=12
        
 
### Other Reference:

https://www.youtube.com/watch?v=hgwBOjJ1kYI

https://en.wikipedia.org/wiki/List_of_HTTP_status_codes

https://umbraco.com/knowledge-base/http-status-codes

https://kinsta.com/blog/http-status-codes/

https://www.dotcom-monitor.com/wiki/knowledge-base/http-status-codes-list/
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        







