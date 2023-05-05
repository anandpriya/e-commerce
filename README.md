

# Use Case:

Suppliers can add products to be sold in Mexico on e-commerce portal. Every product has 1000 attributes including product id.

Kindly provide solution to add products using new design where user will be choosing from the given options to enter information about the product. Data in Database is in English but need to show information on UI in Spanish.


 ## Objectives and Key Results(OKR):
 
 
 ## Functional requirements
 
 The functional requirements of our systems are:
 
 Add product using new design in English and store in English DB
 
 Sync and batch translation in to Spanish of existing ENGLISH product database for Mexico clients and save it in spanish product database
 
 Get product information in spanish as well as in English
 
 ## Non Functional Requirements
 
Service should work with low latency as otherwise, customer experience will suffer.
 
Service should scale easily as we are expecting a good number of hits with regional languages in the future.

Localization/Translation should not alter the exact meaning.

The non-functional requirements of our systems are:
 
 Availability: (Availability % 99.999% (5 nines), Downtime per Year: 5.26 minutes, Downtime per Month: 25.9 seconds, Downtime per Week: 6.05 seconds)
 
 Reliability
 
 Scalability
 
 Performance
 
 Consistency

Maintainability
 
 Fault tolerence
 
 Disaster Recovery
 
 Durability
 
 ## APIs
 
 /add-product/id
 
 /en/get-product/id  >> english
 
 /sp/get-product/id   >> spanish
 

## High Level Design



 
### Solution Diagram



![alt text](https://github.com/anandpriya/e-commerce/blob/main/HLD.png)

Sample Message to translation tool:

{

“string”: “high definition”,

"language id": 5  # for spanish

“translation_flag” : 1

"security token" : "XXGFFHGGJHGKJHk"

}
 
 
 
 ### Flow Diagram
 
### Database design

The following illustration visualizes the data model:

![alt text](https://github.com/anandpriya/e-commerce/blob/main/datamodel.png)


string, translation_id, and translated value.


## Tech Stack

Tech Stack: Node.js, Java, spring boot, Redis, Mongo DB, Kafka, Kafka Connect, docker, kubernetes, application load balancer, third party tool to translate

For Localization of data: Used third party paid System
We have set an SLA of 6 hours with third party system for translation.
