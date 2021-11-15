# Understanding OAuth 2.0 and OpenID Connect

## Stephanie Chamblee

### Description

Learn about the elements that make up the OAuth 2.0 and OpenID Connect protocols to create a secure and seamless authentication experience for your users. Understand how these best practices have impacted modern web development and learn practical steps to using the protocols in your own applications.

Following the OAuth 2.0 framework with the OpenID Connect protocol can enhance your application's security by delegating its authentication management and following the recommended industry best practices for web security. An important step in making sure your application is following these guidelines is understanding why they exist and the problems that they solve. In this talk, we will discuss the context of these protocols, an overview of their concepts, and practical steps to implement authentication in your own app.

### Thoughts

- open standards are best practices and they evolve over time
- if you read and take to heart an RFC, they may change and update over time
- Open web standards
  - SAML
  - OAuth 2.0
  - JWT
  - OIDC

### History of Auth

- 1961 - Password access for each user
  - The first method of authenticating users
  - User -> Password -> Computer
    - Was fine for a while to provide access since you had to physically be there
    - Until the internet
  - Simple login form
    - Password Strength Requirements
      - Libraries to show this
    - Password Hashing
      - Never store plain text passwords
    - MFA (multi-factored-authentication)
      - the user will back up the passwords with another method
  - pwned passwords
    - https://haveibeenpwned.com/
- 2002 - SAML
  - SAML 2.0 - is XML based so it is much more verbose than JSON
  - No way to offer delegated api access at the time
- 2012 - OAuth2
  - Open Authorization Discussion Group
    - Published along with the veritoken spec
  - Delegated Authorization
  - Very quickly OAuth2 began being utilized for things it was not designed for
    - began being used for authentication instead of authorization
      - Authorization - allowing you to get into something - car key, concert ticket
      - Authentication - verifies the identity - passport, cruise cards
  - While authorization can be used from authentication, authorization should not be used for authentication
- OIDC - https://openid.net/connect/
  - Adds information about the user to OAuth2

### Foundation - Terminology

- Four roles
- Authorization grant types
- JWTs
- Four Roles Described by OAuth2
  - Resource Owner
    - Grants access to the protected resource
      - End User
      - Scopes
  - Resource Server (RS)
    - Application Controlling the Data
  - Client
    - Application requesting the data
  - Authorization Server (AS)
    - Application handling delegated authorization decisions

### Tokens

- Three tokens
  - Access Token
    - What the access token wants to get information from the user
  - Refresh Token
    - Allows the client application to continually ask for new user access tokens
  - ID Token
    - used to identify the resource owner - like a driver's license - always going to be JSON Web Tokens
    - for the consumption of the client app
- 3 parts of JWT
  - header
    - algorithm and type (alg & jwt)
  - payload
    - The payload contains the information sent about the user - claims (ddata about the user)
  - signature
    - Uses payload, header an secret and specified algorithm in the header to verify authentic token
- You're not obscuring the data, you are verifying that they were sent by the correct person

### Authorization Grants

- Authorization Code + PKCE (Pixy)
- Device Code
- Client Credentials
- Implicit Flow? - No longer recommended for Single Page Application - Browsers have advanced, so the implicit flow is deprecated
- Confidential vs. Public
  - Secrets
    - Whether or not an application is capable of keeping a secret
    - Confidential Clients are able to keep that secret in a secure way, Public clients can not
- Front-Channel - Browser to API, not as private
- Back-Channel - Server to API, very secure - two backend servers communicating
- In a vast majority of cases you'll be using the Authorization Code + PKCE
  - Web apps, SPAs, and mobile
  - Even recommended for usage with confidential clients
- Client Credentials Flow
  - Back Channel
    - Machine to Machine
    - example: microservices
  - Device Code
    - example: IoT
    - example: command line tool
    - example: raspberry pi, arduino

### OAuth and OIDC Flow

- 1.2 Protocol Flow
- https://oauth.net/2/
  - OAuth docs
- https://auth0.com/docs/
  - auth0 docs
- it is good to be aware of the details of the specification, but it's good to utilize 3rd party libraries to handle a lot of the heavy lifting to abstract away the smaller details
