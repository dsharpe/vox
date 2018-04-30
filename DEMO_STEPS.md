Melbourne Demo

JHipster v4.14.3

Start
* rm -rf vox
* mkdir vox
* cd vox
Microservice
* mkdir catalog
* cd catalog
* jhipster
    * Microservice application
    * Defaults except MySQL dev db
* jhipster entity Product
    * name: String
    * description: String
    * price: BigDecimal
* mvn test [45 seconds]
* mvn -Pprod package dockerfile:build [1 minute] -> slide
Gateway
* cd ..
* mkdir gateway
* cd gateway
* jhipster —experimental [1.5 minutes] -> slide
    * Microservice gateway
    * Defaults except MySQL dev db and React
* jhipster entity Product
    * Y
    * ../catalog
    * Yes, regenerate
* Bugs - remember “experimental” :)
    * Remove SERVER_API_URL in product.reducer.ts
    * Remove 2nd forward slash on line 89 in product.reducer.ts
    * Move FaHdd0 from line 12 to line 14 in header.tsx
    * Remove three spaces before ‘]’ on line 80 in header.tsx
* mvn -Pprod package dockerfile:build [5 minutes] -> slides (2)
Docker Compose
* cd ..
* mkdir docker-compose
* cd docker-compose
* jhipster docker-compose
    * Microservice application
    * ../
    * (a)ll
    * Yes, for logs and metrics with JHipster Console
* docker-compose up -d [2+ minutes] -> slides
URLs
* Gateway - http://localhost:8080
* Registry - http://localhost:8761
* Kibana - http://localhost:5601
    * Dashboard - Open - jvm-dashboard
Scaling
* docker-compose up -d --scale catalog-app=2 [2 minutes] -> slide
Finish
* docker-compose down

