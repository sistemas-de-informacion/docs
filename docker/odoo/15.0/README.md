# Heroku configuration step by step

heroku login
heroku apps:create si2-odoo
heroku addons:create heroku-postgresql:hobby-dev
heroku pg:credentials:url 

Anotar
dbname=d5glkf2ms20stt 
host=ec2-3-223-72-172.compute-1.amazonaws.com 
port=5432 
user=zwqdpojihupukc password=a1233df56b8889f9147205d99389bc636c8d774cc2042f1d0e0a5474149faa4e 
sslmode=require

heroku config:set HOST={{host}}
heroku config:set PORT={{port}}
heroku config:set USER={{user}}
heroku config:set PASSWORD={{password}}
heroku config:set DATABASE={{dbname}}

heroku config:set HOST=ec2-3-223-72-172.compute-1.amazonaws.com
heroku config:set PORT=5432
heroku config:set USER=zwqdpojihupukc
heroku config:set PASSWORD=a1233df56b8889f9147205d99389bc636c8d774cc2042f1d0e0a5474149faa4e
heroku config:set DATABASE=d5glkf2ms20stt


Asegurar que Docker esta arrancadao
heroku container:login 
docker build -t web .
heroku container:push web 
heroku container:release web
