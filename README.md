# aws-solutions-architect-associate-prep
# S3
-Simple Storage Service
-Object Storage-max object size is 5 terabytes
- S3 features
  - Cross Region Replication 
  - Lifecycle Policy
  -Encryption 
  -Static Website Hosting
  
Bucket: a container (web folder) for objects (files) stored in Amazon S3.  They are are global names; meaning there can't be any duplicates with the same name. The containers can contain up to 63 lowercase letters. Each account can have up to 100 buckets per account.

AWS Regions: specific locations that work with S3 buckets. While the S3 buckets can be accessed globally, the S3 bucket can be stored and used in a specific region that you choose. This allows better access and control of your files. The files can be stored in a region that is particular to that region in order to satisfy customer requirements in order to reduce latency, or located in particular region to satisfy data locality and sovereignty concerns; in addition to meeting disaster recovery and compliance needs. You can control the location of your data based on the region unless explicitly copied to another region in another bucket location. 

OBJECTS: the entities stored in the Amazon S3 buckets. An object can store virtually any kind of data in any format. Objects can range from 0 bytes to 5TB per object. Meaning S3 can store virtually an unlimited amount of data. Each object consistst of data and metadta. The data in the object is treated as a stream bytes. It doesn't matter to Amazon what type of data you store and S3 won't act any differently if it was text or binary.
Metadat is associated with an Amazon S3 object is a set of name/value pairs that describe the object. There are two types of metadata: system metadata and user metadata. System metadata is created and used by S3 itself and it includes things like the date last modified, object size, MD5 digest, and HTTP content-type. User Metadata is optional, and it can only be specified at hte time an object was created. You can use custom metadate to tage your data with attributes that are meaningful to you.

Keys: a unique identfier used with an S3 bucket. A key can be up to 1024 bytes of Unicode UTF-8 characters, includeing embedded slashes, backslashes, dots, and dashes. All keys must be unique within a single bucket, but different buckets can contain objects with the same key. The combination of bucket, key, optional version ID uniquely identifies an Amazon S3.

Object URl: S3 is storage for the internet and evety S3 object can be addressed by a unique URL formed using the web services endpoint, the bucket name, and the object key. An example url:
http://mybucket.s3.amazonaws.com/jack.doc
"mybucket" is the name of the S3 bucket name and jack doc is the key or filename,. If another object is created, for instace:
http://mybucket.s3.amazonaws.com/fee/fi/fo/fum/jack.doc
then the bucket name is still mybucket, but now the key or filename is the string fee/ fi/fo/fum/jack.doc. A key may contain delimeter characters like slashes or backslashes to help you name and logically organize your S3 objects, but no S3 it is simpoly a long key name in a flat namespace. There is no actual file or folder hierarchy

S3 Operations:
Create/delete bucket
write an object

