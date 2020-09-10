/*
#LevelDB

LEVELDB is a key value embedded database.
npm install level
`
const level = require("level")
const db = level('./whatever.db');
//this creates a database.
const db = level('./whatever.db',{valueEncoding:'json'}) will allow you to store json instead of binary blocks
`
LEVELDB is good for:
-> using the same db in node and browser.
-> when data is not relational.
-> build your own kappa architecture*.

###Atomicity and Consistency
Either all transactions succeed or all of them fail.
Consistency also ensures that data isn't stuck between two valid states.

It is implemented in LEVELDB as batch.

db.batch([
    {name:'Hamza',age:21},
    {name:'Bruce Wayne',age:55}
],(err)=>{console.err(err);})

If either one of the operations in the array fail then the entire batch is aborted.
*/

