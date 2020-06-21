# learn-oauth
What I learned about oauth

# 3. Introduction
```
OAuth actors (with specific roles) acts in interactional flow
OAuth tokens (credentials) like keys to unlock resources stored securely
OAuth endpoints (Web services, API realized on OAuth server)
OAuth flows (4 different types: mobile app, cloud, web services)
```

# 4. Practical OAuth usage
google linkedin paypal facebook services
provide API services.(protected by OAuth)

## OAuth Worksheets
develop and leverage social services (e.g. Google, Facebook)
```
- Documentation :
    https://developers.google.com/accounts/docs/OAuth2
    https://developers.google.com/oauthplayground/
- Prerequisite : Google Account, curl
- Client Registration
- Authorization Endpoint
- Token EndPoint
- Resources Access
```

# 5. Scenario
```
Resource Owner - Resources Server(GMail) - Resources
               - mobile app(3rd party) from App Store
```

![alt 3rd party](./img/05.3rd.png)

# 8. Password Anti-pattern
providing password (credentials) is dangerous in security perspectives

## Password Anti-pattern Examples
![alt pw anti pattern](./img/08.pwanti.png)
```
Examples of password anti-pattern
1 open mobile app -> owner Sarah credentials verification
saving credentials on mobile device : not secure (other apps can act on behalf of Sarah)

2 cloud example
twitter -> LinkedIn using twitter credentials to create news stream
```
Solve this problem with OAuth2.0 without sharing password.


# 9. Solution : OAuth 2.0
```
Resource Owner - OAuth Server - Resources Server(GMail) - Resources
               - mobile app
```
1. mobile App -> Oauth Server
2. Oauth Server ask Resource owner credentials
   Resource Owner inputs and verifies credentials to OAuth Server
2. Token (randomly created) created by OAuth server (stored in DB)-> mobile App
3. App sends token to Resources Server -> sends back to Oauth Server
4. OAuth Server checks token(check if revoked or granted)
5. Resource Server's own authorization process -> sends Resources to 3rd party app

## OAuth 2.0 Solution

![alt oauth2](./img/09.oauth2sol.png)
```
Delegating access to resources via http protocol : 

Provide token to the app (specific access right. it has an expiration date)
User obtains token by providing credentials(username, pw) to OAuth server (then it sends back the token)

This token is used by mobile app(3rd party) to access resources from Resource Server
(only subset of data for a limited period of time)

OAuth is used for :
Access rights are delegated to third party clients.
```

## Advantages of Oauth 2.0
- First time loggin in OAuth Server: Users are asked for list of information that will be given out.
- App access(Token) can be revoked

# 10. OAuth is Standardized by IETF
```
References to more Information on OAuth 2.0
OAuth 2 is a standard for delegating authorization for accessing resources via HTTP.

OAuth 2 is specified and standardized by the IETF in RFC6749.

http://tools.ietf.org/html/rfc6749
```

# 11. OAuth Components & Terminology

# 12. OAuth Actors