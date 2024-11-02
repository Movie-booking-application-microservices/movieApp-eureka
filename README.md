Movi-Bookign app
- we have 3 microservices: user-app, theatre-app, movie-app
- config-server: configuration related details which movie service is using
- eureka-client and eureka-server: for service discovery and service registry. Simply by knowing the service name and not having to worry about the uri details. So we have used service 
name like USER-SERVICE and THEATRE-SERVICE and eureka automaticatlly discovers their uri for us. In the image below we can see all the instances registered on eureka and can be discovered
 img:
![image](https://github.com/user-attachments/assets/c911933f-043a-4944-b864-e177cc0bdbad)

api-gateway service: 
It sits in front of a collection of services(that is configured in its route), acting as a single point of entry for all of them. Using API Gateway url to send request to movie app:
![image](https://github.com/user-attachments/assets/35ac1feb-edcb-4eed-a071-3e21f24b1ae8)

