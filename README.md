# docker-mongodb_auth

    docker run --name mymongo --restart=always -d -p 27017:27017 mongo mongod --auth

    sudo docker exec -i -t mymongo bash
    mongosh

or


    docker exec -it mymongo mongosh
    use admin

    db.createUser({user:"mymongo_admin",pwd:"mymongo_password",roles:[{role:"root",db:"admin"}]})

    mongodb://mymongo_admin:mymongo_password@SERVER_IP

    db.createUser({
      user: 'my_prod',
      pwd: 'my_prod_password',
      roles:[
        { 
          role: 'readWrite',
          db: 'prod_myweb'
        }
      ]
    })
