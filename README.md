- how to test security protected services:

```
$ curl -iu13888888888:123456 -d "" http://54.223.95.220:31400/auth
HTTP/1.1 200 OK
x-auth-token: 5f31eb56-66ba-4aa6-82e9-171bdbcffbf2

$ curl -i -H "x-auth-token: 2e576bd5-6d44-41c7-9ce4-532aca8e3718" http://54.223.95.220:31400/orders/1
HTTP/1.1 200 OK

{"orderId":"1","productId":"product-id-1"}
```