# Backend-Interview-Question
CAP Theorem:~
The CAP theorem states that it is not possible to guarantee all three of the desirable properties – consistency, availability, and partition tolerance at the same time in a distributed system with data replication. 

The theorem states that networked shared-data systems can only strongly support two of the following three properties: consistency, availability and partial tolerance.


PACELC theorem:~

The PACELC theorem is an extension to the CAP theorem. It states that in case of network partitioning (P) in a distributed computer system, one has to choose between availability (A) and consistency (C) (as per the CAP theorem), but else (E), even when the system is running normally in the absence of partitions, one has to choose between latency (L) and consistency (C).

Q. What is meant by eventual consistency?
Ans. Eventual Consistency is a guarantee that when an update is made in a distributed database, that update will eventually be reflected in all nodes that store the data, resulting in the same response every time the data is queried

Q. What do you mean by strong consistency?
Ans. Strong Consistency simply means the data must be strongly consistent at all times. All the server nodes across the world should contain the same value as an entity at any point in time. And the only way to implement this behavior is by locking down the nodes when being updated. 
Q. What are the different types of databases?
Ans. https://www.matillion.com/resources/blog/the-types-of-databases-with-examples 

Q. What are message queues used for?
Ans. Message queues allow different parts of a system to communicate and process operations asynchronously. A message queue provides a lightweight buffer which temporarily stores messages, and endpoints that allow software components to connect to the queue in order to send and receive messages.

Q. What is the purpose of a reverse proxy?
Ans. A reverse proxy ultimately forwards user/web browser requests to web servers. However, the reverse proxy server protects the web server's identity. This type of proxy server also moves requests strategically on behalf of web servers, typically to help increase performance, security, and reliability.

Q. What is TLS and how does it work?
Ans. Transport Layer Security (TLS) encrypts data sent over the Internet to ensure that eavesdroppers and hackers are unable to see what you transmit which is particularly useful for private and sensitive information such as passwords, credit card numbers, and personal correspondence.

Q. What is Docker? Why do we use it?
Ans. Docker is an open source containerization platform. It enables developers to package applications into containers—standardised executable components combining application source code with the operating system (OS) libraries and dependencies required to run that code in any environment.

Q. What are webhooks used for?
Ans. A webhook is a lightweight API that powers one-way data sharing triggered by events. Together, they enable applications to share data and functionality, and turn the web into something greater than the sum of its parts. APIs and webhooks both allow different software systems to sync up and share information.

Q. Which service by Amazon Web Services (AWS) can you use for Queues?

Ans. Amazon Simple Queue Service (SQS)

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

Q. What does Pub Sub mean?
Ans. Publish/subscribe messaging
Publish/subscribe messaging, or pub/sub messaging, is a form of asynchronous service-to-service communication used in serverless and microservices architectures. In a pub/sub model, any message published to a topic is immediately received by all of the subscribers to the topic.

Q.What is S3 Service in AWS? What is the AWS S3 service used for?
Ans. Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

Q. What is EC2 Instance in AWS?

Ans. An Amazon EC2 instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure.

Q. What is Cloudfront in AWS?

Ans. Amazon CloudFront is a web service that speeds up distribution of your static and dynamic web content, such as . html, . css, . js, and image files, to your users. CloudFront delivers your content through a worldwide network of data centres called edge locations.


Q. What is Route 53 In AWS?

Ans. Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service. It is designed to give developers and businesses an extremely reliable and cost effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.

Q. What are ELBs in AWS?

Ans. Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs).

# Node.js Interview Questions
Q. What is the difference between readFile and readFileSync?
Ans. s.readFile takes a call back which calls response.send as you have shown - good. If you simply replace that with fs.readFileSync, you need to be aware it does not take a callback so your callback which calls response.send will never get called and therefore the response will never end and it will timeout.

You need to show your readFileSync code if you're not simply replacing readFile with readFileSync.

Also, just so you're aware, you should never call readFileSync in a node express/webserver since it will tie up the single thread loop while I/O is performed. You want the node loop to process other requests until the I/O completes and your callback handling code can run.

Q. What does process in node.js mean?
Ans. The process object in Node. js is a global object that can be accessed inside any module without requiring it. There are very few global objects or properties provided in Node. js and process is one of them. It is an essential component in the Node.



Q. What is Node.js? Where can you use it?
Ans. Node.js is an open-source, cross-platform JavaScript runtime environment and library to run web applications outside the client’s browser. It is used to create server-side web applications.

Node.js is perfect for data-intensive applications as it uses an asynchronous, event-driven model. You can use  I/O intensive web applications like video streaming sites. You can also use it for developing: Real-time web applications, Network applications, General-purpose applications, and Distributed systems.

Q. Why use Node.js?
Node.js makes building scalable network programs easy. Some of its advantages include:

It is generally fast
It rarely blocks
It offers a unified programming language and data type
Everything is asynchronous 
It yields great concurrency


Q. What is the difference of JS from browser to JS on node.js
Ans. ( https://medium.com/swlh/what-is-node-js-and-how-does-it-differ-from-a-browser-ddebef00cbd9#:~:text=Unlike%20the%20browser%20where%20Javascript,can%20execute%20software%20and%20more )

Q. Write three different ways to reverse a string in Javascript? a. using inbuilt method, b. iteratively, c. recursively
Ans. ( https://www.freecodecamp.org/news/how-to-reverse-a-string-in-javascript-in-3-different-ways-75e4763c68cb/ )

Q. Write a program to check two objects are equal ( deep equal )
Ans. https://www.samanthaming.com/tidbits/33-how-to-compare-2-objects/

Q. Explain some areas where you have seen currying being implemented in React / other libraries?
Ans. https://blog.logrocket.com/understanding-javascript-currying/#:~:text=Currying%20is%20a%20checking%20method,that%20can%20handle%20one%20responsibility

Q. IIFE ?
Ans. https://www.javascripttutorial.net/javascript-immediately-invoked-function-expression-iife/ 

Q. How does Node.js work?
A web server using Node.js typically has a workflow that is quite similar to the diagram illustrated below. Let’s explore this flow of operations in detail.

Node.js Architecture Workflow

Clients send requests to the web server to interact with the web application. Requests can be non-blocking or blocking:
Querying for data
Deleting data 
Updating the data
Node.js retrieves the incoming requests and adds those to the Event Queue
The requests are then passed one-by-one through the Event Loop. It checks if the requests are simple enough not to require any external resources
The Event Loop processes simple requests (non-blocking operations), such as I/O Polling, and returns the responses to the corresponding clients
A single thread from the Thread Pool is assigned to a single complex request. This thread is responsible for completing a particular blocking request by accessing external resources, such as computation, database, file system, etc.

Once the task is carried out completely, the response is sent to the Event Loop that sends that response back to the client.

Q. Does Node.js improve throughput? Why/How?
Ans. https://www.quora.com/Does-Node-js-improve-throughput-Why-How


Q. How do you explain throughput?
Ans. Throughput, in business, is the amount of a product or service that a company can produce and deliver to a client within a specified period of time. The term is often used in the context of a company's rate of production or the speed at which something is processed.

Q. How is Node js having high IO throughput?
Ans. ( https://javascript.plainenglish.io/understanding-nodejs-performance-dc9f2673455e )

Q. What are examples of CPU intensive tasks?
Ans. Sorting, search, graph traversal, matrix multiply are all CPU operations, a process is CPU-intensive or not it depends on how much and how frequent are their execution.

Q. How can you end up blocking your main thread in node.js?
Ans. ( https://www.geeksforgeeks.org/how-node-js-overcome-the-problem-of-blocking-of-i-o-operations/ )

Q. What is the event loop?
Ans. ( https://medium.com/@mmoshikoo/event-loop-in-nodejs-visualized-235867255e81#:~:text=The%20Event%20Loop%20sees%20that,(2)%20is%20being%20executed.&text=So%20the%20delay%20parameter%20in,which%20the%20function%20is%20executed )

Q. Phases of event loop?
Ans. ( https://medium.com/@kunaltandon.kt/process-nexttick-vs-setimmediate-vs-settimeout-explained-wrt-different-event-loop-phases-c0506b12921d#:~:text=The%20different%20phases%20of%20an,phase%20of%20the%20event%20loop )

Q. What is process.tick?
Ans. ( https://medium.com/@amanhimself/how-process-nexttick-works-in-node-js-cb327812e083 )

Q. When can process.tick starve your event loop?
Ans. ( https://medium.com/dkatalis/eventloop-in-nodejs-settimeout-setimmediate-vs-process-nexttick-37c852c67acb )

( https://www.youtube.com/watch?v=9RhOGoChGqo )

Q. What is the difference between setTimeout and setInterval?
Ans. The only difference is , setTimeout() triggers the expression only once while setInterval() keeps triggering expression regularly after the given interval of time.

( https://medium.com/@monica1109/scheduling-settimeout-and-setinterval-ca2ee50cd99f#:~:text=The%20only%20difference%20is%20%2C,the%20given%20interval%20of%20time )

Q. How can you make a network request with http module from the backend?
Ans. ( https://medium.com/edureka/node-js-requests-6b94862307a2 )

Q. How can you create your own events?
Ans. ( https://www.freecodecamp.org/news/how-to-code-your-own-event-emitter-in-node-js-a-step-by-step-guide-e13b7e7908e1/ )

Q. What are clusters?
Ans. A sharded cluster in MongoDB is a collection of datasets distributed across many shards (servers) in order to achieve horizontal scalability and better performance in read and write operations.
( https://medium.com/@phoenixm103/creating-mongo-cluster-9578be417d16#:~:text=A%20MongoDB%20cluster%20is%20sharded,the%20nodes%20of%20the%20shard )

Q. How does your Node.js application handle scale? Elaborate
Ans. ( https://www.freecodecamp.org/news/scaling-node-js-applications-8492bd8afadc/ )

Q. What are CORS? How do you configure them? Why do you need them?
Ans. https://auth0.com/blog/cors-tutorial-a-guide-to-cross-origin-resource-sharing/ 

Q. What is rate limiting?
Ans. Rate limiting is a strategy for limiting network traffic. It puts a cap on how often someone can repeat an action within a certain timeframe – for instance, trying to log in to an account. Rate limiting can help stop certain kinds of malicious bot activity. It can also reduce strain on web servers. However, rate limiting is not a complete solution for managing bot activity.
https://www.cloudflare.com/en-in/learning/bots/what-is-rate-limiting/

Q. How does middleware work in express?
Ans. Middleware functions are functions that have access to the request object ( req ), the response object ( res ), and the next function in the application's request-response cycle. The next function is a function in the Express router which, when invoked, executes the middleware succeeding the current middleware.

https://medium.com/@adamzerner/middleware-in-express-60d75055ba8f 

Q. What is the difference between Encryption and Hashing?
Ans. Since encryption is two-way, the data can be decrypted so it is readable again. Hashing, on the other hand, is one-way, meaning the plaintext is scrambled into a unique digest, through the use of a salt, that cannot be decrypted.
( https://medium.com/swlh/the-difference-between-encoding-encryption-and-hashing-878c606a7aff#:~:text=%2D%20Encryption%20is%20a%20process%20to,into%20a%20fixed%2Dlength%20string )

Q. What is the difference between https and http?
Ans. Http vs https protocol
To summarize, HTTP delivers data and all files ( HTML, images, queries, etc) on the World Wide Web. HTTPS has been around since the very beginning of the internet. It has not received its fair share of attention until recently but that does not undermine the role it plays. As we learnt earlier, S stands for secure

( https://medium.com/@pallavimodi/http-https-what-is-the-difference-3a97fe2f7fd8#:~:text=To%20summarize%2C%20HTTP%20delivers%20data,on%20the%20World%20Wide%20Web.&text=HTTPS%20has%20been%20around%20since,earlier%2C%20S%20stands%20for%20secure )

Q. What is TLS?
Ans. https://medium.com/talpor/ssl-tls-authentication-explained-86f00064280#:~:text=TLS%20is%20a%20protocol%20for,the%20content%20of%20the%20messages 

Q.What is AES?
Ans. AES is a block cipher: it will receive 128 bits of text which will be transformed to obtain a different 128 bits of encrypted data. But 128 bits or 16 characters most probably won't be enough to fit all the data we wish to encrypt, so how does AES manage to encrypt whole documents filled up with text.
( https://medium.com/quick-code/understanding-the-advanced-encryption-standard-7d7884277e7#:~:text=AES%20is%20a%20block%20cipher,documents%20filled%20up%20with%20text%3F )

Q. What is JWT Token? Why do we need to use JWT? What are some pros and cons?
Ans. JWT : It is a definitely a clever way to securely get the identity of the client. In simple language there is a secret Key used to encrypt the JSON formatted Data which primarily includes the user-id. Now an encryption of data with the Key generates the token that is sent to the client and used in every request.
Ans. https://medium.com/@rahulgolwalkar/pros-and-cons-in-using-jwt-json-web-tokens-196ac6d41fb4#:~:text=JWT%20%3A%20It%20is%20a%20definitely,and%20used%20in%20every%20request

Q. What is salting? Where do we store salt?
Ans. https://medium.com/swlh/introduction-to-salted-hashed-passwords-d19bd6f92480#:~:text=A%20salt%20is%20a%20random,hashing%20function%20with%20a%20salt 

Q. What is V8?
Ans. https://medium.com/@duartekevin91/basics-of-understanding-chromes-v8-engine-c5c8ec61fa6b 

Q. What is difference between JS on the browser and node?
Ans. Unlike the browser where Javascript is sandboxed for your safety, node. js has full access to the system like any other native application. This means you can read and write directly to/from the file system, have unrestricted access to the network, can execute software and more.

https://medium.com/swlh/what-is-node-js-and-how-does-it-differ-from-a-browser-ddebef00cbd9#:~:text=Unlike%20the%20browser%20where%20Javascript,can%20execute%20software%20and%20more 

Q. What is the difference between Authorisation and Authentication?

Ans. Simply put, authentication is the process of verifying who someone is, whereas authorization is the process of verifying what specific applications, files, and data a user has access to. The situation is like that of an airline that needs to determine which people can come on board.

https://www.sailpoint.com/identity-library/difference-between-authentication-and-authorization/#:~:text=Simply%20put%2C%20authentication%20is%20the,people%20can%20come%20on%20board 




# MongoDB interview Questions
There are two types of data as we know – (i) structured data and (ii) unstructured data. 
Structured data is usually stored in a tabular form whereas unstructured data is not. 
To manage huge sets of unstructured data like log or IoT data, a NoSQL database is used.

What is MongoDB?
MongoDB is an open-source NoSQL database written in C++ language. It uses JSON-like documents with optional schemas. 
It provides easy scalability and is a cross-platform, document-oriented database.
MongoDB works on the concept of Collection and Document.
It combines the ability to scale out with features such as secondary indexes, range queries, sorting, aggregations, and geospatial indexes.
1. What are some of the advantages of MongoDB?
Some advantages of MongoDB are as follows:
MongoDB supports field, range-based, string pattern matching type queries. for searching the data in the database 
MongoDB support primary and secondary index on any fields
MongoDB basically uses JavaScript objects in place of procedures
MongoDB uses a dynamic database schema
MongoDB is very easy to scale up or down
MongoDB has inbuilt support for data partitioning (Sharding).
2. What is a Document in MongoDB?
A Document in MongoDB is an ordered set of keys with associated values. It is represented by a map, hash, or dictionary. In JavaScript, documents are represented as objects:
{"greeting" : "Hello world!"}
Complex documents will contain multiple key/value pairs:
{"greeting" : "Hello world!", "views" : 3}
5. What is the Mongo Shell?
It is a JavaScript shell that allows interaction with a MongoDB instance from the command line. With that one can perform administrative functions, inspecting an instance, or exploring MongoDB. 
The mongos acts as a query router, providing an interface between client applications and the sharded cluster.
Q. What are SQL Databases? What are some companies who use Mongo, what type of applications are these?
Ans. https://medium.com/@rsk.saikrishna/when-to-use-mongodb-rather-than-mysql-d03ceff2e922

Q. What is the difference between SQL and NoSQL databases?
Ans. SQL is used for managing data that has many schemas and relations. NoSQL is a non-relational database that does not require a fixed schema and is easy to scale. These databases are sometimes also referred to as “Not Only SQL” databases. With NoSQL, data can be stored in a schema-less, any data can be stored in any record.

https://medium.com/dot-intern/nosql-vs-sql-which-is-better-1abe3a6db268#:~:text=SQL%20is%20used%20for%20manage%20data%20that%20has%20many%20schemas%20and%20relations.&text=NoSQL%20is%20a%20non%2Drelational,be%20stored%20in%20any%20record
https://www.mongodb.com/nosql-explained/nosql-vs-sql

Q. What are some features of MongoDB?
Ans. https://www.upgrad.com/blog/mongodb-real-world-use-cases/

Q. What are aggregate queries in mongodb?
Ans. https://www.mongodb.com/what-is-mongodb/features 

Q. What are aggregate queries in mongodb?
Ans. Aggregation groups documents in a collection and is used to provide results like the total number of documents, sum, average, maximum and minimum values. To the people who are acquainted with SQL the aggregation stages of MongoDB are analogous to COUNT(), SUM(), GROUP BY, LIMIT etc of SQL's

https://medium.com/@ashiqgiga07/aggregation-in-mongodb-209515e5b0ba#:~:text=Aggregation%20groups%20documents%20in%20a,BY%2C%20LIMIT%20etc%20of%20SQL's

Q. What are pipelines in aggregation?
Ans. https://medium.com/mongodb-performance-tuning/explaining-aggregation-pipelines-2d1edd46a341

An aggregation pipeline consists of one or more stages that process documents: Each stage performs an operation on the input documents. For example, a stage can filter documents, group documents, and calculate values. The documents that are output from a stage are passed to the next stage.

Q. How do you do aggregate queries?
Ans. https://www.idera.com/glossary/aggregate-query 

Q. How can you group by a particular value in MongoDB?
Ans. https://www.mongodb.com/docs/manual/reference/operator/aggregation/group/ 

Q. How can you paginate on MongoDB?
Ans. https://www.educba.com/mongodb-pagination/ 


Q. How can you sort in MongoDB?
Ans. https://www.tutorialspoint.com/mongodb/mongodb_sort_record.htm#:~:text=To%20sort%20documents%20in%20MongoDB,is%20used%20for%20descending%20order 


Q. What is indexing in MongoDB? Why do we need to use indexing? What are pros and cons for indexing?
Ans. https://medium.com/@irfan.ali_65238/indexes-in-mongodb-df227ca95ce0

Q. Write the query for indexing a field in MongoDB?
Ans. https://www.mongodb.com/docs/manual/reference/method/db.collection.createIndex/ 

Q. What is the improvement in performance in MongoDB?
Ans. Other ways to improve MongoDB performance after identifying your major query patterns include: Storing the results of frequent sub-queries on documents to reduce read load. Making sure that you have indices on any fields you regularly query against. Looking at your logs to identify slow queries, then check your indices.

https://www.mongodb.com/basics/best-practices#:~:text=Other%20ways%20to%20improve%20MongoDB,queries%2C%20then%20check%20your%20indices

Q. What is the data structure used for indexing?
Ans. The db. collection. createIndex() method only creates an index if an index of the same specification does not already exist. MongoDB indexes use a B-tree data structure.

Q. Are values sorted in indexes? Are indexes sorted?
Ans. Indexing is a way of sorting a number of records on multiple fields. Creating an index on a field in a table creates another data structure which holds the field value, and a pointer to the record it relates to. This index structure is then sorted, allowing Binary Searches to be performed on it.


Q. What are Replica Sets in MongoDB?
Ans. A replica set in MongoDB is a group of mongod processes that maintain the same data set. Replica sets provide redundancy and high availability, and are the basis for all production deployments. This section introduces replication in MongoDB as well as the components and architecture of replica sets.

https://medium.com/swlh/mongodb-creating-a-3-node-replica-set-cluster-7ca94849b139#:~:text=By%20the%20end%20of%20this,maintain%20the%20same%20data%20set

Q. Explain the structure of ObjectID in MongoDB.

Ans. An ObjectId in MongoDB is a 12-byte BSON type. In the 12-byte structure, the first 4 bytes of the ObjectId represent the time in seconds since the UNIX epoch. The next 3 bytes of the ObjectId represent the machine identifier. The next 2 bytes of the ObjectId represent the process ID.

Q. By default, which index is created by MongoDB for every collection?
Ans. MongoDB creates a unique index on the _id field during the creation of a collection. The _id index prevents clients from inserting two documents with the same value for the _id field.
Q. In which format MongoDB represents document structure?
Ans. In MongoDB, data is stored as documents. These documents are stored in MongoDB in JSON (JavaScript Object Notation) format.

Q. What is the limitation of a document in MongoDB?

Ans. The maximum BSON document size is 16 megabytes. The maximum document size helps ensure that a single document cannot use excessive amount of RAM or, during transmission, excessive amounts of bandwidth. To store documents larger than the maximum size, MongoDB provides the GridFS API.

https://www.mongodb.com/docs/manual/reference/limits/#:~:text=The%20maximum%20BSON%20document%20size,MongoDB%20provides%20the%20GridFS%20API

Q. What is the difference between MongoDB and Redis database?

Ans. MongoDB is a document-oriented, disk-based database optimised for operational simplicity, schema-free design and very large data volumes. Redis is an in-memory, persistent data structure store that enables developers to perform common operations with minimal complexity and maximum performance.
https://www.geeksforgeeks.org/difference-between-redis-and-mongodb/#:~:text=Redis%20offers%20memory%20efficiency%2C%20fast,(i.e.%20NoSQL)%20database%20program 

Q. How can you add references between multiple collections?
Ans. https://www.mongodb.com/docs/manual/reference/database-references/ 

Q. What are lookups in aggregation for MongoDB?
Ans. https://medium.com/cameoeng/mongodb-lookups-and-populates-an-unexpected-journey-940e08e36a94 

Q. What are graph lookups?
Ans. Definition. $graphLookup. Performs a recursive search on a collection, with options for restricting the search by recursion depth and query filter.

Q. What is the alternative for lookups in MongoDB?
Ans. https://www.mongodb.com/community/forums/t/how-to-properly-utilize-lookup-with-alternate-join-conditions/14701
