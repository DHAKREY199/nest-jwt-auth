Curl for getting JWT Token : 

curl --location 'https://nest-jwt-auth-w4sg.onrender.com/auth/token' \
--header 'Content-Type: application/json' \
--data-raw '{"email": "himanshu@gmail.com"}'

Curl for validating JWT Token 

curl --location 'https://nest-jwt-auth-w4sg.onrender.com/auth/validate' \
--header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImhpbWFuc2h1QGdtYWlsLmNvbSIsInN1YiI6MSwiaWF0IjoxNzYzODEwOTg2LCJleHAiOjE3NjM4MTEyODZ9.ozR61juwOVfLBPQ1VirqFeGsEeNakJ-Q9yIA7_jUhpc'
