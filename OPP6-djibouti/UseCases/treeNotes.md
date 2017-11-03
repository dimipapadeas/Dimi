Use cases dependency tree:



UCS-015: Establish federated authentication via a trusted Identity Provider
req: -
(we consider it universal all the systems )


### Regional data sharing hub\s use cases (RDSH):
UCS-018: Provide reliable & highly-available pub-sub messaging infrastructure
req: -
( the pub-sub infrastructure )

UCS-001: Upload new datasets
req:015
(user must be able to authenticate himself)

UCS-002: Create a Python script to check for 3SD for automatic detection of "bad data" from incoming sources.
req: -
(no req)

UCS-003: Use the local web application to automatically generate/edit most of HTML content of the dataset page
req:001
req:002

UCS-004: The dataset`s HTML page automatically generates CSV visualization in the form of a graph
req:003

UCS-005: Enhances HTML pages with JSON-LD information related to Google and AWISC
req:003
req:019 // AWISC
## ????????????????????????????????? mhpws kanei req to 6


UCS-006: Register site-map with AWISC
req:019
{ UCS-006 =the infrastructure  to be able to de indexed by req 20 it must registered first .. it requires the existence of AWISc  }



### Omar`s use cases:

UCS-018:reliable & highly-available pub-sub messaging infrastructure
req-a auth only..

UCS-016: Create Automatic Weather Station queues (AWS)
req:001
req:018
```
{ 
##    TODO CHECK AGAIN...
       Automatic Weather Station
    Mouktar is keen to automate the collection of data so that he can receive more regular observations- once per hour. 
  
    Mouktar ask Omar to create a new queue for this AWS. As this raw data is not intended to be publicly available, there is no need to publish Web pages for commercial search engines to crawl, nor for the AWS data to be registered with the Authoritative WIS Catalogue.

    QControl script:
     subscribes to the data from the queue, and checks the values. If an erroneous value is detected, an email is sent to Mouktar notifying him of the anomaly, 
     else the script places the data on the 
     ** official queue **
      for observation data from Assa Gaïla, which is then automatically propagated to other subscribers (such as Mariam) and to the CSV dataset.

}
```

UCS-013: Create dissemination queues of an uploaded dataset
## req:016 ???? or 01 // den pernei input apo to AWSqueues???
req:018

UCS-014: Monitor dissemination queues of an uploaded dataset
req:013


Authoritative WIS Catalogue\s use cases (AWISC):

UCS-019: Maintain a cataloge of official WIS datasets
req auth mechanism



UCS-020: Periodically crawl registered pages and update internal index
req:005 //requires 19
req:006( covers req:019)
## (update internal index = indirectly updates RDSH queues data??? )???????????????????????????check again


UCS-021: Provide a dataset search page
req:20
## mhpws kai to 14???????????????????????????

UCS-022: Provide a dataset search (REST) API
req:20


UCS-023: Has its site-map registered in Google search
req:020
(+ 005  covered)
(UCS-023= enables indexing by Google bots)




Mariam use cases:

UCS-007: Discover weather observation dataset queues (using Google/AWISC)
req:021 
req:023
+ QUEUES?? ??????????????????????RECHECK
## (finds observations via AWISC (21) or via Google Search(23) )  


UCS-008: Subscribe to weather observation dataset queues
req:007
(covered reqs authenticated, discovery, queues  )


UCS-009: Request re-send of missed notifications
req:007
(covered reqs authenticated, discovery, queues  )


Daves use cases:

UCS-010: Search for weather observations registered in AWISC via the AWISC web application
req:021
(covered reqs authenticated, discovery )


UCS-011: Search for weather observations registered in AWISC via the AWISC web services
req:022
(covered reqs authenticated api usage.. )



Mohameds use cases:

UCS-012: Discover observation data via Google Search
req:023
(covered by 023: Has its site-map registered in Google search)

Delly`s use cases:


UCS-017: Upload fresh data automatically via web application
( to kanei mesw AWS + RDSH)

req:016
(Covered by UCS-016: Create Automatic Weather Station queues (AWS))
