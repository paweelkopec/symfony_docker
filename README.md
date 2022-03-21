# Environment:

docker-compose up -d --build

List: 

``curl --location --request GET 'http://localhost:8080/product?firstResult=0&maxResults=10&order=name&sort=asc'``

Add new: 

`curl --location --request POST 'http://localhost:8080/product' \
 --header 'Authorization: Basic YWRtaW46YWRtaW4=' \
 --header 'Content-Type: application/json' \
 --data-raw '{
     "name": "Smart VPS",
     "description": "Sample VPS azya1",
     "price": "100.88",
     "currency": "PLN"
 }'`
 
 Update
 
 `curl --location --request PUT 'http://localhost:8080/product/43' \
  --header 'Authorization: Basic YWRtaW46YWRtaW4=' \
  --header 'Content-Type: application/json' \
  --data-raw '{
      "name": "Smart VPS test",
      "description": "Sample VPS azya test",
      "price": "900.88",
      "currency": "USD"
  }'`
 
Read:

`curl --location --request GET 'http://localhost:8080/product/43'` 

Delete: 

`curl --location --request DELETE 'http://localhost:8080/product/1' \
 --header 'Authorization: Basic YWRtaW46YWRtaW4='`
 
 
