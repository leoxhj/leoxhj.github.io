# Mongo Note

TBD

# Connections
mongo ip:port/dbName -u user -p password
mongo 10.25.154.4:27017/admin -u mongo -p mongo
  
# Query examples
1. query last document
`db.action_execution_d_b.find({}).sort({start_timestamp:-1}).limit(1)`
2. query with logical operator
`db.action_execution_d_b.find({$or: [ { start_timestamp: { $gte: 1514251905782270 } }, { end_timestamp: { $gte: 1514251905782270 } } ] })  `
3. query count
`db.action_execution_d_b.find({}).count()`


# Remove
1. delete all documents from a collection

`db.action_execution_d_b.remove({})`


# Security 
1. Built-in Roles

`dbAdmin, dbOwner(readWrite+dbAdmin+userAdmin), userAdmin, clusterAdmin, clusterManager,clusterMonitor`

