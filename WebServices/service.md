#Web services

##Key of web services
- Designed for machine-to-machine(or application-to-application) interaction
- Should be interoperable - Not platform dependent
- Should allow communication over a network

##Service Definition
- Request/Response format(XML/JSON/..)
- Request Structure
- Response structure
- Endpoint

###How does data exchange between applications take place?
- through request and Response

###How can we make web services platform independent?
- by creating platform independent request and responses by using data exchange format JSON/XML

###How does application know the format of request and response?
- we provide a service definition

###SOAP
- XML structure
- SOAP-ENV:Envelop (SOAP-ENV:Header + SOAP:ENV:Body)
- SOAP definition: WSDL(Web service definition language)

###REST
- Make best of HTTP: Hyper Text Transfer Protocol
![HTTP](../image/http.PNG)
- No restriction on data exchange format
- transport: only http
- Service Definition: No standard .WADL/Swagger

####REST VS SOAP
- Restrictions VS Architectural Approach
- Data Exchange format
- Service definition
- transport
- Ease of implementation
