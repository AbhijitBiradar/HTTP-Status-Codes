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












