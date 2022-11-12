# spring-security-jwt

Below steps to test this code.<br/>
Step-1 generate jwt token<br/>
curl --request POST \
  --url http://localhost:8080/authenticate \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: 920b1368-4da2-a5c4-a252-d1d1661fe84e' \
  --data '{\n	"username" : "foo",\n	"password" : "foo"\n}'

Step-2 replace <jwt token> below with generated jwt token in above step.<br/>
  curl --request GET \
  --url http://localhost:8080/hello \
  --header 'authorization: Bearer <jwt token>' \
  --header 'cache-control: no-cache' \
  --header 'content-type: application/json' \
  --header 'postman-token: cd64f700-8b32-d75f-cf7c-88cec15ccaca'
