

# Use Case:

Suppliers can add products to be sold in Mexico on e-commerce portal. Every product has 1000 attributes including product id.

Kindly provide solution to add products using new design where user will be choosing from the given options to enter information about the product. Data in Database is in English but need to show information on UI in Spanish.


 ## Objectives and Key Results(OKR):
 
OBJECTIVE: Be Proactive with Supplier Success

Key Results:

Implement new "add product" platform to provide more acurate and structured input form based on customer asks and latest trends


OBJECTIVE: Implement Scalable, high performing, easy to maintain product management system

Key Results:


Objective: Increase online sales by 20%

Key results:

●     Increase traffic in Mexico e-commerce portal by 25% as buyers/ visitors prefer local language content

●     Increase number of orders value by 5%


Objective: Improve Net promoter scores (NPS) for suppliers

Key results:

●     Increase in number of suppliers by 10%

●     Increase in number of prodcuts added by 10%



Objective: Improve Customer effort scores(CES) for buyers

Key results:

●    Reduce time to select the product to buy as information shared is more accurate, structured and relevant

Objective: Minimize codebase framework dependencies


Key Result: Decrease codebase frameworks from 5 to 2
 
 
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

Same data model will be in Spanish as well.

Enumeration List:

Based on new "add product" design, create enum list for each category, like setting possible values for each attribute of product. Examples:

Model	

	A
 
	B
 
	C
	
Color	

	Red
 
	Blue
 
	Others
 
 






## Tech Stack

Tech Stack: Node.js, Java, spring boot, Redis, Mongo DB, Kafka, Kafka Connect, docker, kubernetes, application load balancer, third party tool to translate

For Localization of data: Used third party paid System
We have set an SLA of 6 hours with third party system for translation.
