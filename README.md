# mongointro
```
db.blogs.insertMany([
{
createdAt: new Date(),
title: "title_1",
text: "text",
author: "author",
lastModified: new Date(),
categories: ["category"],
id: "12345",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_2",
text: "text_2",
author: "author_2",
lastModified: new Date(),
categories: ["category_2"],
id: "12345_2",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_3",
text: "text_3",
author: "author_3",
lastModified: new Date(),
categories: ["category_3"],
id: "123453",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_4",
text: "text_4",
author: "author_4",
lastModified: new Date(),
categories: ["category"],
id: "123454",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_5",
text: "text_5",
author: "author_5",
lastModified: new Date(),
categories: ["category"],
id: "123455",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_6",
text: "text_6",
author: "author_6",
lastModified: new Date(),
categories: ["category_6"],
id: "123456",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_7",
text: "text_7",
author: "author_7",
lastModified: new Date(),
categories: ["category_7"],
id: "123457",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_8",
text: "text_8",
author: "author_8",
lastModified: new Date(),
categories: ["category_8"],
id: "123458",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_9",
text: "text_9",
author: "author_9",
lastModified: new Date(),
categories: ["category"],
id: "123459",
objectId: ObjectId(32),
},
{
createdAt: new Date(),
title: "title_10",
text: "text_10",
author: "author_10",
lastModified: new Date(),
categories: ["category_10"],
id: "1234510",
objectId: ObjectId(32),
},
])

db.blogs.insertOne({
createdAt: new Date(),
title: "title_11",
text: "text_11",
author: "author_11",
lastModified: new Date(),
categories: ["category_11"],
id: "44545",
objectId: ObjectId(32)
})

db.blogs.findOne({author: "author_11"});
db.blogs.find({objectId: {$gt: ObjectId(5)}});
db.blogs.find({createdAt: {$gt: ISODate("2022-04-01")}});
db.blogs.find({lastModified: {$exists: true}});
db.blogs.find({createdAt: {$type: "date"}});
db.blogs.update({lastModified: {$exists: false}}, {$set: {lastModified: new Date()}});
db.blogs.update({createdAt: {$gt: ISODate("2022-05-01")}}, {$push: {categories: "lorem"}});
db.blogs.find({categories: "voluptas"}, {$pull: "voluptas"});
db.blogs.remove({categories: "corrupti"});
db.blogs.find();
```
