# microservices

Let's invoke the request through the Zuul API Gateway. We use the following URL: http://localhost:8765/{application-name}/{uri}. The port 8765 is the default port for the Zuul API Gateway server.

1. Access exchange service through zuul
	http://localhost:8765/currency-exchange-service/currency-exchange/from/EUR/to/INR

	Direct access exchange service use below url,
	http://localhost:8000/currency-exchange/from/EUR/to/INR
	
2. Access currency converter service through zuul

	http://localhost:8100/currency-converter-feign/from/USD/to/INR/quantity/1000
	
	
Run microservices steps:

Step 1: Run the netflix-eureka-naming-server.

Step 2: Run the currency-exchange-service on port 8000.

Step 3: Run the currency-conversion-service on port 8100.

Step 4: Run the netflix-zuul-api-gateway-server.

Step 5: Open the browser and invoke the URL http://localhost:8761. It shows all the services that are registered with the Eureka naming server.