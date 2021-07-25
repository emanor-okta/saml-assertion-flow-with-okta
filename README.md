# Sample SAML Assertion Flow

This example shows how to use the [Okta SAML Assertion Flow](https://developer.okta.com/docs/guides/implement-saml2/overview/) to exchange an assertion for tokens.
The application uses the Okta Emabed Link of a SAML Application to start an IdP Initiated flow. The SSO URL for the SAML application points to this application which will strip out the SAML Assertion, and then use it in a /token call to OKta.  

The application is already configured to use a preconfigured Okta Org. To view the configurations in Okta login to https://dev-96797994-admin.okta.com.  
Credentials  
Username: `read.only`  
Password: `Th1sPassword`  

Relevant Settings:
* Security -> Identity Providers -> SAML Assertion Flow IdP
* Applications -> Applications -> SAML Assertion Flow - IDP
* Applications -> Applications -> SAML Assertion OIDC Flow


### To Install
```
git clone https://github.com/emanor-okta/saml-assertion-flow-with-okta.git
cd saml-assertion-flow-with-okta
go mod tidy
```

### To Run
```
go run main.go
```  

Navigate to http://localhost:8080   
Click `Get Tokens` to start the flow.

