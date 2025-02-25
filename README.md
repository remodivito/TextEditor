# The QUBEditron3000
This project involves developing a secure, reliable, modular, possibly over-engineered text editor. It features a variety of functions using different programming languages and technologies, each hosted as an independent microservice, containerised with Docker and orchestrated with Kubernetes: 
* A 'period count' function, developed with Dart
* A 'whitespace stripping' function, developed with Go
* A 'palindrome checking' function, developed with Python
* A 'longest word function', developed with C#.
* 'Save text' and 'Get text' functions, developed with Javascript and hosted with Google Cloud Functions

All microservices feature a comprehensive suite of CI unit testing, implemented with a suitable testing framework for each language.  
The microservices are found on the cluster by a reverse proxy with a unique key for each microservice; when a function is requested, the reverse proxy will check the cluster to see if the function is available, and route the HTTP requests and responses accordingly.
The reverse proxy also allows for the addition and configuration of microservices via an API endpoint.  

The 'monitoring_metrics' directory includes a service monitoring dashboard which performs live tests of the microservices and the reverse proxy, and updates the dashboard with results. It emails the admin (me) whenever a microservice goes down or does not function as expected.  

The text editor:  
<img width="451" alt="image" src="https://github.com/user-attachments/assets/7ac38716-6501-4a4d-adf3-e79d68dff22e" />  

The monitoring and metrics dashboard:  
<img width="451" alt="image" src="https://github.com/user-attachments/assets/e314a31a-b0a1-42bd-8793-f1c0400b5ea7" />  
