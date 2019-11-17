# learn-oauth
What I learned about oauth

```
OAuth actors acts in interactional flow
OAuth tokens (credentials) like keys to unlock resources stored securely
OAuth endpoints (Web services, API realized on OAuth server)
OAuth flows 
```

## OAuth Worksheets
develop and leverage social services (e.g. Google, Facebook)
```
- Documentation  & Prerequ
- Client Regist
- Authorization Endpoint
- Token EndPoint
- Resources Access
```

## Scenario
```
Resource Owner - Resources Server(GMail) - Resources
               - mobile app(3rd party) from App Store
```

## Password Anti-pattern
providing password (credentials) is dangerous in security perspectives

## Solution : OAuth 2.0
```
Resource Owner - OAuth Server - Resources Server(GMail) - Resources
               - mobile app
```
1. owner input and verify credentials to OAuth Server
2. token created by OAuth server
3. token to Resources Server
4. OAuth Server checks token(check if revoked or granted)
5. Resource Server own authorization process -> sends resources to 3rd party app

## Password Anti-pattern Examples
```
1
open mobile app -> owner credentials verification
saving credentials on mobile device is not secure (other apps can act on behalf of Sarah)

2
cloud example
twitter -> LinkedIn news stream
```
Solve this problem with password anti-pattern without sharing password

## OAuth 2.0 Solution
```
provide token to the app (specific access right. it has an expiration date)
user obtains token by providing credentials to OAuth server (then it sends back the token)
this token is used by mobile app(3rd party) to access resources from Resource Server

OAuth is used for :
Access rights are delegated to third party clients.
```

## OAuth is Standardized by IETF
```
References to more Information on OAuth 2.0
OAuth 2 is a standard for delegating authorization for accessing resources via HTTP.

OAuth 2 is specified and standardized by the IETF in RFC6749.

http://tools.ietf.org/html/rfc6749 (opens in new tab).
```


## OAuth Components & Terminology
