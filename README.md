# SSRF-demo
Simple flask app to demonstrate Server-Side Request Forgery (SSRF) vulnerabiliry and attack

# OWASP Reference
https://owasp.org/www-community/attacks/Server_Side_Request_Forgery

# How can I use the ssrf-demo app?

Here some use cases:
* Educating developers on SSRF risk and impact
* Self-learning
* Lunch and learn sessions

# Requirements
```
pip3 install Flask
pip3 install requests
```

# How to use
The "/fetch" route accepts both GET and POST requests. You can pass the URL in the `url` query parameter as a GET request, http://localhost:5000/fetch?url=http://target-url.com or as  POST in the request body as `url=http://target-url.com`

## Example:
```
GET request: 
curl http://localhost:5000/fetch?url=http://target-url.com

POST request: 
curl -X POST -d "url=http://target-url.com" http://localhost:5000/fetch
```

# Keep in mind
This is a vulnerable app. Don't use it in a production enviornment.
