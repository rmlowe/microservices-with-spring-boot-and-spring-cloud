# RESTful Web Services

## Social Media Application Resource Mappings

### User -> Posts

- Retrieve all Users      - GET  /users
- Create a User           - POST /users
- Retrieve one User       - GET  /users/{id} -> /users/1
- Delete a User           - DELETE /users/{id} -> /users/1

- Retrieve all posts for a User - GET /users/{id}/posts
- Create a posts for a User - POST /users/{id}/posts
- Retrieve details of a post - GET /users/{id}/posts/{post_id}

## Error in the Log
```
Resolved exception caused by Handler execution:




- This happened because there were no getters in HelloWorldBean class

## Questions to Answer

- What is dispatcher servlet?
- Who is configuring dispatcher servlet?
- What does dispatcher servlet do?
- How does the HelloWorldBean object get converted to JSON?
- Who is configuring the error mapping?

- Mapping servlet: 'dispatcherServlet' to [/]

- Mapped "{[/hello-world],methods=[GET]}" onto
public java.lang.String com.in28minutes.rest.webservices.restfulwebservices.HelloWorldController.helloWorld()
- Mapped "{[/hello-world-bean],methods=[GET]}" onto
public com.in28minutes.rest.webservices.restfulwebservices.HelloWorldBean com.in28minutes.rest.webservices.restfulwebservices.HelloWorldController.helloWorldBean()
- Mapped "{[/error]}" onto
public org.springframework.http.ResponseEntity<java.util.Map<java.lang.String, java.lang.Object>> org.springframework.boot.autoconfigure.web.servlet.error.BasicErro
- Mapped "{[/error],produces=[text,html]}" onto
public org.springframework.web.servlet.ModelAndView org.springframework.boot.autoconfigure.web.servlet.error.BasicErrorController.errorHtml(javax.servlet.http.Http





























































































#### Internationalization

##### Configuration
- LocaleResolver
   - Default Locale - Locale.US
- ResourceBundleMessageSource

##### Usage
- Autowire MessageSource
- @RequestHeader(value = "Accept-Language", required = false) Locale locale
- messageSource.getMessage("helloWorld.message", null, locale)




























































































































}
```

### Versioning
 - Media type versioning (a.k.a. “content negotiation” or “accept header”)
   - GitHub
 - (Custom) headers versioning
   - Microsoft
 - URI Versioning
   - Twitter
 - Parameter versioning
   - Amazon
 - Factors
   - URI Pollution
   - Misuse of HTTP Headers
   - Caching
   - Can we execute the request on the browser?
   - API Documentation
 - No Perfect Solution

#### More
- https://www.mnot.net/blog/2011/10/25/web_api_versioning_smackdown
- http://urthen.github.io/2013/05/09/ways-to-version-your-api/
- http://stackoverflow.com/questions/389169/best-practices-for-api-versioning