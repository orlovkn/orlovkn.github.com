установка
https://www.digitalocean.com/community/tutorials/how-to-install-mongodb-on-ubuntu-20-04-ru
https://docs.mongodb.com/manual/tutorial/install-mongodb-on-red-hat/#configure-the-package-management-system-yum

sudo systemctl start mongod

команды
http://flash2048.com/post/mongoDB-shell

офиц дока
https://docs.mongodb.com/manual/tutorial/


> db
test
> use demo
switched to db demo
> db
demo


db.students.insert({firstName: "Василий", lastName: "Пупкин", age: 19, hobby: ["футбол", "хоккей"] })

db.getCollectionNames()

> db.test.find()
> db.test.update({status: 'ok'}, {status: 'failed'})


> db.createCollection('logs')
{ "ok" : 1 }
> show collections
logs
> 
> db.logs.find()
> 
> db.logs.insert({"entity": "some"})
WriteResult({ "nInserted" : 1 })
> db.logs.find()
{ "_id" : ObjectId("60100c04498d731f56471e7a"), "entity" : "some" }
> db.logs.remove({entity: "some"})
WriteResult({ "nRemoved" : 1 })




use admin
db.createUser(
  {
    user: "goswebcontrolleradmin",
    pwd: "goswebcontrollerpass12345",
    roles: [ { role: "userAdminAnyDatabase", db: "admin" }, 
             { role: "dbAdminAnyDatabase", db: "admin" }, 
             { role: "readWriteAnyDatabase", db: "admin" } ]
  }
)


> use gwcontroller
switched to db gwcontroller
> show collections
> db.createCollection('logs')
{ "ok" : 1 }
> show collections
logs
> 


> show dbs
admin                 0.000GB
companydb             0.000GB
config                0.000GB
goswebcontrollerlogs  0.000GB
gwcontroller          0.000GB
local                 0.000GB
students              0.000GB
test                  0.000GB
> 


db.collection.remove()
db.ProcessorLog.remove({})


db.dropDatabase()

> db.logs.find({'channel':'app'}).pretty()
