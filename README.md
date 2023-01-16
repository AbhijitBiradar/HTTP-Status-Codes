# HTTP-Status-Codes

1. **What are HTTP status codes?**

    HTTP status codes are three-digit responses from the server to the browser-side request. Everyone has probably gotten the classic 404 page-not-found error. That is an HTTP client error status code and there are a lot more of them.

    These status codes (also called response status codes) serve as a means of communication between the server and the internet browser and there are multiple code classes based on the type of information they are communicating. The differences in classes are indicated through the first digit of the error code, for example: just like a 404, any other 4xx will mean that in some way the page or website could not be reached, while a 2xx means that your request was successfully completed.


2. **How are HTTP status codes categorized?**

    HTTP status codes are split into 5 different categories. Each category will give you hints as to what the response was, even if you don't know the specific response code.

    For an explanation of each category - and each individual status code - click on the corresponding link below or go to our complete list of HTTP status codes.

    1xx - Informational: The server has received the request and is continuing the process 

    2xx - Successful: The request was successful and the browser has received the expected information 

    3xx (Redirection): You have been redirected and the completion of the request requires further action

    4xx (Client Error): The website or the page could not be reached, either the page is unavailable or the request contains bad syntax 

    5xx (Server Error): While the request appears to be valid, the server could not complete the request


3. **1XX Status Codes**

    A 1XX-level status code tells you that the request you’ve made to the server is still in progress for some reason. This isn’t necessarily a problem, it’s just extra information to let you know what’s going on.

    A 1xx Informational status code means that the server has received the request and is continuing the process. A 1xx status code is purely temporary and is given while the request processing continues. For most tasks you won't encounter these much, as it's not the final response to the request.


    **Status Code 100: “Continue.”** 

        This means that the server in question has received your browser’s request headers, and is now ready for the request body to be sent as well. This makes the request process more efficient since it prevents the browser from sending a body request even though the headers have been rejected.


    **Status Code 101: “Switching protocols.”**  

        Your browser has asked the server to change protocols, and the server has complied.


    **Status Code 102: "Processing".** 

        The 102 Processing status code means that the server has accepted the full request but has not yet completed it and no response is available as of  yet.
        An interim response used to inform the client that the server has accepted the complete request but has not yet completed it.


    **Status Code 103: “Early hints.”**  

        This returns some response headers before the rest of the server’s response is ready.
        The 103 Early hints status code is intended to be used to allow the user agent to preload resources, while the server prepares a response. It is intended to be primarily used with the Link Header.


    **Reference**
    
        https://www.youtube.com/watch?v=_B93xM5TPuI&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=1
      
        
        
4. **2XX Status Codes**    
       
        A 2xx Succesful status code means that the request was successful and the browser has received the expected information. This is generally the one you want to see, as it means that the request was a success and has been received, understood and accepted it. As a website owner you should make sure that all pages and resources (images, videos, etc.) all return a 2xx status code. This means that browsers can reach it successfully and that your website visitors can see and use your website.


     **Status Code 200: "Everything is OK.".**

        The 200 OK status code means that the request was successful, but the meaning of success depends on the request method used


     **Status Code 201: "Created".** 

        A 201 Created status code is like a 200 OK status code, however, a 201 status code means that a request was successfully processed, and it returned, or created, a resource or resources in the process. A 201 status code is typically used for PUT requests. For example, when a PUT request is used, a new resource is created on the URL specified in the request. If there is a 201 status code in a POST request, it means a resource was created at a different API endpoint/location.


     **Status Code 202: “Accepted”.** 

        The 202 Accepted status code means that the server has received a request for processing, and it is been accepted, but the request has not been completed. It also does not mean the request will eventually be accepted, as it will depend on when the actual processing takes place. This type of request is typically seen in APIs where a batch process is run once a day. Since there is no way for HTTP to communicate after a request has succeeded or user’s connection has been closed, an API might send off an email to a user notifying them that the process has


     **Status Code 203: “Non-Authoritative Information”.** 

        The 203 Non-Authoritative Information status code is typically used by an HTTP proxy or third party. The proxy, sitting between the client and server may change the responses before reaching the client. To indicate that something was changed during the process, a status code 203 is used. However, the drawback of this method is that it is not possible to know what the original status code was if a proxy changed something in the response. A suggested workaround is to use a warning header along with a 214 status code, which is used to indicate that there was a change or modification in the response. Using the warning header allows the original status code to passed through


     **Status Code 204: “No Content”.** 

        A status code of 204 indicates that the response has been successfully delivered by the server and fulfilled and no further content is to be sent in the body of the response. As an example, if the request is sent in the form on a page, once the response is sent, the client/browser is not supposed to change the view, meaning the form should not be refreshed or direct users to a new page. No additional content should be replaced or appear in terms of the user’s perspective
        
     **Status Code 205: “Reset Content”.** 
        
        Like the 204 No Content status code, a status code 205 Reset Content indicates that the server has sent the request successfully and requires the user agent to refresh/reset the view to its original state. If we use the example of a form on a page, once the user completes and submits the form, the client/browser should clear the form back to its original state so a user can take further action. A 205 status code assumes no further content will be provided.
        
        
     **Status Code 206: “Partial Content”.** 
        
        A 206 Partial Content status code can be used for a variety of requests and typically indicates that the server has fulfilled a partial request for a resource. For example, if a client is only looking for a specific portion, or range, of a specific resource or page. Another example of where a 206 status code is used is in video. A client may only load video in pieces as to not have to wait for the video to buffer or load, helping to avoid a negative user experience where a user would have to wait longer before the video plays. This is normal best practice among HTTP video players to avoid bandwidth and perceived latency issues.


    **Reference**
        
        https://www.youtube.com/watch?v=Q-0Rd-la7PQ&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=2


5. **3XX: Redirection** 

        The 3xx status codes are used in cases of URL redirection. Websites are always changing and evolving, so there may be times where marketers need to direct users to an updated, or different page. Redirects help alleviate users from having to search for what they are looking for and maintain your ranking in search engines. The redirect actions may be carried out by the browser automatically or may require additional interaction from users. The 3xx HTTP status codes are vital for SEO (Search Engine Optimization) and user experience, as well as tell search engines what content you want them to crawl and index. If not properly implemented, users may be directed to an unintended location, which could result in a 4xx status code and could affect SEO quality scores.


    **Status Code 300: “Multiple Choices.”**

         Sometimes, there may be multiple possible resources the server can respond with to fulfill your browser’s request. A 300 status code means that your browser now needs to choose between them. This may occur when there are multiple file type extensions available, or if the server is experiencing word sense disambiguation.

        The 300 Multiple Choices status code indicates that a resource has moved and can redirect to multiple locations. In this case the user must decide which resource to use. The server may indicate a preferred choice and that should be indicated in the header field where the user agent could redirect to the preferred choice automatically. In practical use, this status code is rarely used as there is no standardized way to choose from multiple responses. See RFC7231, Section 6.4.1 for more information. 
        
    **Status Code 301: Moved Permanently**

        “The requested resource has been moved permanently.” This code is delivered when a web page or resource has been permanently replaced with a different resource. It is used for permanent URL redirection.

         A 301 Moved Permanently status code is utilized to indicate that a target resource has been moved to a permanent location. The 301 status code tells the browser/client to use this new location or URL going forward in the header. Along with the 301 status code, the new URL will be given in the response as well as update any URLs in the previous location(s), along with updating to the new URL. See RFC7231, Section 6.4.2 for more information.


    **Status Code 302: Found**
    
        “The requested resource has moved, but was found.” This code is used to indicate that the requested resource was found, just not at the location where it was expected. It is used for temporary URL redirection.

        A 302 Found status code indicates to a client/browser that a resource that they are accessing is temporarily located under a different location. Unlike the 301 status code, a 302 status code indicates a temporary move, so the client should not automatically update its links to the new location, as again, it is meant to be temporary. An example of where the 302 status code should be used if there are multiple URLs, but they could be served in different languages. A user may arrive at specific URL, but the client may redirect them automatically to the proper page based on their browser settings and use this on subsequent visits. It is noted that in some cases, browsers may change a request from POST to GET. In the case that this action is not favorable, a 307 status code should be used. See RFC7231, Section 6.4.3 for more information.  


    **Status Code 303: See Other**
    
        Understanding a 303 status code requires that you know the difference between the four primary HTTP request methods. Essentially, a 303 code tells your browser that it found the resource your browser requested via POST, PUT, or DELETE. However, to retrieve it using GET, you need to make the appropriate request to a different URL than the one you previously used.

        A status code 303 See Other indicates that a server will be redirecting the client/browser to another resource. The resource will be indicated as a URL the header field. Unlike the 301 and 302 status codes, it does not mean a resource has temporarily or permanently move, its intent is to specify the URL to where the response to the specific request can be found via a GET request. 303 status codes should not be cached, however, the response to the subsequent request may be cached. A typical use of the 303 status code would be to ensure users do not accidentally resubmit form data via a POST request. They should be directed to a new page. If not, they may unknowingly click the back button in their browser, which may ask them to resubmit again, which leads to unnecessary duplicate submissions. See RFC7231, Section 6.4.4 for more information.  
        
        
    **Status Code 304: Not Modified**
    
        “The requested resource has not been modified since the last time you accessed it.” This code tells the browser that the resources stored in the browser cache haven’t changed. It’s used to speed up web page delivery by reusing previously-downloaded resources.

        A status code of 304 Not Modified is sent in response to a conditional GET or HEAD request. Clients/browsers can send a conditional request, such as If-Match, If-None-Match, If-Modified-Since, If-Unmodified-Since, or If-Range, asking if a specific resource has been modified since a specific date/time. This is done only if the client has previously accessed, downloaded, and saved the resource. If it has been modified since that specific date/time last accessed, the server will return a 200 OK status code. If it has not been changed since that date/time, the 304 status code is sent as the response, indicating that the saved resource should be served since it has not been modified since the last time it was accessed. See RFC7232, Section 4.1 for more information.         
        
        
    **Status Code 305: Use Proxy**
    
        The 305 Use Proxy status code is a deprecated status code that is no longer used due to security consideration. It was used to indicate to a client that the resource they were accessing must be accessed via a proxy. For more information on the 305 Use Proxy status code, see RFC7231, Section 6.4.5         
        
        
    **Status Code 306: Unused**
    
        Like the 305 status code, the 306 Unused status was originally known as Switch Proxy. The 306 status code was used in a previous specification. Its intention was to be used as in indication to the client that subsequent requests to a resource should use the proxy that was specified. This was deemed as a security issue, so it is no longer used. For more information on the 306 Unused status code, see RFC7231, Section 6.4.6        
        
        
    **Status Code 307: “Temporary Redirect.”**
    
        This status code has replaced 302 “Found” as the appropriate action when a resource has been temporarily moved to a different URL. Unlike the 302 status code, it does not allow the HTTP method to change.

        Like the 302 Found redirect status code, the 307 Temporary Redirect status code indicates to the client/browser that a resource or document is available at a different, temporary URL and returns that URL. Since the redirection is temporary and could change, the browser/client should continue to access the current URL for subsequent requests. The main difference between the 302 status code and the 307 status code is that the 307 status code does not allow changing requests from a POST request to a GET request, so if the client requested POST request, it be redirected and initiate the POST request again. See RFC7231, Section 6.4.7          
        
        
    **Status Code 308: “Permanent Redirect.”**
    
        The 308 status code is the successor to the 301 “Moved Permanently” code. It does not allow the HTTP method to change and indicates that the requested resource is now permanently located at a new URL.

        A 308 Permanent Redirect status code is a cacheable status code (unless cache controls are implemented) that indicates that a target resource is now located at a permanent URL and subsequent requests should be directed to that URL as well. Additionally, the client should update any old bookmarks to the new location. The 308 status code is very similar to the 301 status code, however, if a 308 status code is sent, the client has to initiate and send the same request on the target location. A 301 status code does not have to do this. Most browsers/clients change the POST request to a GET request. See RFC7238, Section 3 for more information.         
        
        
     **Reference**    

        https://www.youtube.com/watch?v=cGXRK6xVUGw&list=PLoqCAsfoCubrObEWVK2zHtdb5D-YUv9G5&index=11

        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        
        







