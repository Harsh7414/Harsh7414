//mongodb Query
slip 1
> db.student.count({marks:{$gt:80}})
b) > db.student.find({marks:{$lt:40}})
c) > var my=db.student.find({marks:{$gt:70}});
> while(my.hasNext()){print(tojson(my.next()));}
d)>db.student.find({gender:"female",$or:[{city:"pune"},{city:"mumbai"},{marks:{$lt:50}}
]})


slip 2
a)> db.product.find().pretty()
b) > db.order.find({Totalbill:{$lt:10000}})
c) > db.order.find({stetus:"in process"})
d) >db.order.find({custName:"arunkumar",stetus:"processed"})

Slip 3
a)> db.publisher.find({city:"mumbai"})
b)> db.book.find({cost:{$lt:1000}})
c) > db.book.find({author:"raguramkrishna",published:2017})
d)> >
db.publisher.find({pname:"OReilly",$or:[{language:"English"},{language:"marathi"}]})

slip 4
a) > db.Hospital.find({Specialization:"Pediatric"})
b)>db.Hospital.find({Hname:"CCC","Doctor.Visit":"Tuesday"})
c)>db.Hospital.find({Specialization:{$not:{$size:1}},"Doctor.Dname":"XXX"})
d) > db.Hospital.find({"People.Rating":{ $gt: 3 },Hname:"AAA"})


slip 5
a) >db.post.find({tag:"food"})
b) >db.post.find({pname:"Amit"})
c) > db.post.find({tag:"travel",pdate:{"$lte":new Date("2018-03-
11")},"user.name":"sagar","user.comment":"like"})
d) > db.post.find({$or:[{"user.cdate":{$lte:new Date("2019-08-07")}},{"user.like":0}]})

slip 6
a) >db.turisum.find({name:"veena word"}).pretty()
b) >db.turisum.find({}).sort({"rate":-1}).limit(1)
c)>db.tour.aggregate([{"$sort":{"year":1}},{"$limit":3},{$group:{_id:null,"count":{"$sum"
:"$expense"}}}])
d) > db.tour.find({destination:"shillong"})

slip 7
a) > db.scien.find({ lname: { $regex: /n/ } })
b) > db.scien.find({BOD:{"$gt":new Date("1950-03-11")},DOD:"still alive"})
c)>db.scien.aggregate([{$group:{_id:{year:"$award.year",Name:"$award.name"}}}])
d) >db.scien.find({"award.name":"turingmachine","award.year":{$lt:1980},field:{$size:4}})

slip 8
a) > db.item.find({status:"D","warehouse.quntity":{$gt:30}})
b) > db.item.find({"tag":{$size:3}})
c) >db.item.find({$or:[{status:"A"},{"warehouse.quntity":{$lt:30},height:{$gt:10}}]})
d) > db.item.find({itemName:"planner",instack:{$lt:20}})

Slip 9
a) > db.transaction.find({customerName:"john"})
b) > db.transaction.find({paymentmode:"debitcard"})
c)>db.transaction.aggregate([{$match:{"paymentmode":"creditcard"}},{$group:{_id:null,
"count":{"$sum":"$payment"}}}])
d)
>db.transaction.aggregate([{$group:{_id:"$paymentmode","count":{"$sum":"$payment
"}}}])

slip 10
a) >db.shopping.find({"model.ram":"3GB","model.rom":"32GB"})
b) > db.custome.find({modelname:"samsung j6"})
c) > db.shopping.aggregate([{"$sort":{"rate":-
1}},{"$limit":1},{$group:{_id:"$brandname"}}])
d) > db.custome.find().sort( { "cname": 1 } )
