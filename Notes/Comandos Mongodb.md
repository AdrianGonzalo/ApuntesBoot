# Comandos Mongodb

## show databases / show dbs
With this command we can see all the mongo databases

## bd.dropDatabase()
With this command we can delete the database we are in

## use 'database selected'
With this command we can switch the database

## db.'colection'.insertOne({...})
With this command we can create colection

## db.'colection'.find()
With this command we can view in

## db.'colection'.createIndex({ email: 1}, {unique: true})
With this command we create a rule so that only one email can be registered, without repeating

## db.'collection'.getIndexes()
With this command we can see all the rules of the collection

## db.'collection'.dropIndex('x')
With this command we can delete the selected rule

## db.'collection'.deleteOne({_id: ObjectId('x')})
With this command we cand delete one object

## db.'collection'.updateOne({ _id: x}, {$set: {password: ' x'}})
With this command we can change the param