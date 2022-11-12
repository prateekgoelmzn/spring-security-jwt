# spring-security-jwt

Below steps to test this code.<br/>
Step-1 generate jwt token<br/>
curl --request POST \
  --url http://localhost:8080/authenticate \
  --header 'content-type: application/json' \
  --data '{\n	"username" : "foo",\n	"password" : "foo"\n}'

Step-2 replace <jwt token> below with generated jwt token in above step.<br/>
  curl --request GET \
  --url http://localhost:8080/hello \
  --header 'authorization: Bearer <jwt token>' \
  --header 'content-type: application/json' \
