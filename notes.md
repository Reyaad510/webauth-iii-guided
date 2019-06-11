JWT
authroizes username and password and sends back token(JWT). Alternative than using sessions and more industry standard. Statles JWT is faster bcux doesnt have to look up session anywhere. Server knows, no lookup needed. Good with horizontal scaling
Session the server will look up if session is valid so user will be let in .
A token you can change content of token

Header: Paylod with two pieces of info. Contains type and algorhythm to sign the token

{
    "alg": "HS256",
    "typ": "JWT"
}

payload has info specific to authorization like user id, user role, etc.

{
  "userId": 1,
  "role": "admin",
  "iat": 1560203144,
  "exp": 1560206744
}

Signature is first two parts of token concatanated together and even a secret strinfg and hashes them to create a signature


// PROJECT

yarn add jsonwebtoken
yarn add dotenv