\# 01 - gRPC Overview



\## 1. What is RPC?

* RPC is a communication ways to call a function or methods that locating at another server and get response from it.
* RPC will help to hides low level networks details
* RPC flow: Clients calls a local procedure -> Marshalling stage: all inputs parameter will be packed into a bytes message -> The packed message will be sent across the network to the server -> The server stub unpacks the message into objects and call the server procedure -> the server run the procedure and the result will be packed up -> the server stub send the result back and the client sub unpack it



\## 2. What is gRPC?

* gRPC is a RPC framework that designed by google.
* gRPC employs Protocol Buffer for serialization and HTTP/2 
* gRPC have 4 types of streaming:

  * Unary: one request made then one answer given ( same as REST )
  * Client Streaming: The client send to server a stream of requests and receives one answer
  * Server Streaming: The client send to server one request and receives stream of answer 
  * Binary: The client send to server stream of request and stream of answer



\## 3. What problem does gRPC solve?

* Faster Performance: can allow multiple requests and responses transmitted over a single TCP connection by HTTP/2 rather than many in HTTP/1.1 => lower latency and increase efficiency
* Language support
* Interoperability

\## 4. How does gRPC work?

* 

\## 5. When should we use gRPC?

* When we have microservice
* When it is bilanguage project
* When the system need fast response and high performance (gaming, streaming, bank)
* The application needs streaming communication (chatting apps)





\## 6. When should we not use gRPC?

* When it is public api (because it will be hard to read, debug and test)
* Simple application



\## 7. What is Protocol Buffer

* Is a method for serializing structured data developed by Google, language neutral, platform neutral
* 



\## 8. Compare REST and gRPC

||REST|gRPC|
|-|-|-|
||||
||||



\## 9. Compare HTTP/1.1 and HTTP/2.2



||HTTP/1.1|HTTP/2|
|-|-|-|
|Data Format|Text (JSON)|Binary (Protocol Buffer)|
|Connection|Multiple TCP connections needed|Normally one TCP conneciton|
|Request|Sequential|Multiplexing|
|Headers|plain text full request|Compressed using HPACK|
|Performance|Slower|Faster|
|Used by|REST API|Modern browser, gRPC|



\## 10. Compare JSON and Protocoal Buffer



\## 11. Interview Summary



\## 12. Self-check Questions

