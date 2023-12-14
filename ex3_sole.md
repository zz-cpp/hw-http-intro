What is the effect of adding additional URI parameters as part of the POST route?

answer:

What is the effect of changing the name properties of the form fields?

answer: 
    the key will change coresponding to the changement.


Can you have more than one Submit button? If you do, how does the server tell which one was clicked? (Hint: experiment with the attribtues of the <submit> tag.)

answer：
    1. EMAIL=fdfd&password=fdfd&secret_info=secret_value&login=Log+In%21
    2. EMAIL=&password=&secret_info=secret_value&login=Log+In_3%21EMAIL=fdfd&password=fdfd&secret_info=secret_value&login=Log+In%21

    the {login: Login+In} is different from {login: Log+In_3}

    <input type="submit" name="login" value="Log In_2!">
    <input type="submit" name="login" value="Log In_3!">

Can the form be submitted using GET instead of POST? If yes, what is the difference in how the server sees those requests?

answer: 
    yes;
    lack request body;
 

What other HTTP verbs are possible in the form submit route? Can you get the web browser to generate a route that uses PUT, PATCH, or DELETE?

answer: 
    
    PUT: GET /?EMAIL=&password=&secret_info=secret_value&login=Log+In%21 HTTP/1.1
    ```HTTP
    GET /?EMAIL=&password=&secret_info=secret_value&login=Log+In%21 HTTP/1.1
    Host: localhost:8081
    Connection: keep-alive
    sec-ch-ua: "Google Chrome";v="119", "Chromium";v="119", "Not?A_Brand";v="24"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Linux"
    Upgrade-Insecure-Requests: 1
    User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
    Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
    Sec-Fetch-Site: cross-site
    Sec-Fetch-Mode: navigate
    Sec-Fetch-User: ?1
    Sec-Fetch-Dest: document
    Accept-Encoding: gzip, deflate, br
    Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,zh-TW;q=0.7,en-GB;q=0.6,en-US;q=0.5
    ```
    PATCH: 
    ```http
    GET /?EMAIL=&password=&secret_info=secret_value&login=Log+In%21 HTTP/1.1
    Host: localhost:8081
    Connection: keep-alive
    sec-ch-ua: "Google Chrome";v="119", "Chromium";v="119", "Not?A_Brand";v="24"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Linux"
    Upgrade-Insecure-Requests: 1
    User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
    Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
    Sec-Fetch-Site: cross-site
    Sec-Fetch-Mode: navigate
    Sec-Fetch-User: ?1
    Sec-Fetch-Dest: document
    Accept-Encoding: gzip, deflate, br
    Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,zh-TW;q=0.7,en-GB;q=0.6,en-US;q=0.5
    ```
    DELETE:
    ```HTTP
    GET /?EMAIL=&password=&secret_info=secret_value&login=Log+In%21 HTTP/1.1
    Host: localhost:8081
    Connection: keep-alive
    sec-ch-ua: "Google Chrome";v="119", "Chromium";v="119", "Not?A_Brand";v="24"
    sec-ch-ua-mobile: ?0
    sec-ch-ua-platform: "Linux"
    Upgrade-Insecure-Requests: 1
    User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/119.0.0.0 Safari/537.36
    Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
    Sec-Fetch-Site: cross-site
    Sec-Fetch-Mode: navigate
    Sec-Fetch-User: ?1
    Sec-Fetch-Dest: document
    Accept-Encoding: gzip, deflate, br
    Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,zh-TW;q=0.7,en-GB;q=0.6,en-US;q=0.5
    ```

    I ask chatGpt and maybe it is not allowed to use PATCH , DELETE ...... in HTML form. It only take effect using JS or other language.

        
