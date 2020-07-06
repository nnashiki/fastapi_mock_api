# fastapi_mock_api
FastAPIで固定値を返すmockAPI

## 環境構築

```
docker build -t fastmock .
docker run -p 8080:80 --rm --name fastmock fastmock
```

## GET POST

GET
```
curl --include http://localhost:8080/items/1 
```

POST
```
curl -X POST -H "Content-Type: application/json" -d '{"id":1,"name":"new_item"}' --include http://localhost:8080/items
```

## 参考
https://fastapi.tiangolo.com/deployment/#docker
https://fastapi.tiangolo.com/tutorial/body/#request-body
