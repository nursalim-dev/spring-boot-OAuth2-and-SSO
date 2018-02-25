<h3>Aplikasi Spring Boot OAuth2 Demo</h3>
<hr/>
Aplikasi Terdiri dari :
<ul>
<li>1. Spring-Cloud-OAuth2-SSO</li>
<li>2. demo-integrated-angular</li>
</ul>
<br/>
# A1. Spring Cloud OAuth2 SSO : Dependencies
 
<ul>
<li>Web</li>
<li>JPA (Java Persistence Api)</li>
<li>MySQL DB</li>
<li>Cloud OAuth2</li>
<li>Cloud Security</li>
</ul>

# A2. Spring Cloud OAuth2 SSO : Run File

```

$ mvn clean spring-boot:run
```

<br/>
cara mendapatkan token
<br/>


```

$ curl -X POST -vu clientGojekApp:mysecret 'http://localhost:10000/oauth/token?username=dickanirwansyah&password=rootroot&grant_type=password'
```

<br/>
mendapatkan token
<br/>


```
* Hostname was NOT found in DNS cache
*   Trying 127.0.0.1...
* Connected to localhost (127.0.0.1) port 10000 (#0)
* Server auth using Basic with user 'clientGojekApp'
> POST /oauth/token?username=dickanirwansyah&password=rootroot&grant_type=password HTTP/1.1
> Authorization: Basic Y2xpZW50R29qZWtBcHA6bXlzZWNyZXQ=
> User-Agent: curl/7.35.0
> Host: localhost:10000
> Accept: */*
> 
< HTTP/1.1 200 
< X-Content-Type-Options: nosniff
< X-XSS-Protection: 1; mode=block
< Cache-Control: no-cache, no-store, max-age=0, must-revalidate
< Pragma: no-cache
< Expires: 0
< X-Frame-Options: DENY
< Cache-Control: no-store
< Pragma: no-cache
< Content-Type: application/json;charset=UTF-8
< Transfer-Encoding: chunked
< Date: Sun, 25 Feb 2018 01:49:26 GMT
< 
* Connection #0 to host localhost left intact
{"access_token":"bdbaddb6-56a8-45fc-9c9c-21df9eb5e30a","token_type":"bearer","refresh_token":"7dbf98ec-2977-4a64-995d-cf0305061c2e","expires_in":34828,"scope":"read write"}
```




