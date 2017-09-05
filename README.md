# Analytics API project description

## Project Overview 
Implement an Web service which provides an HTTP API for accessing some analytic metrics.   
### Objective
Import provided data into database and implement an web service which will calculate and send back some analytical metrics based on input arguments via some defined API.
### Technical Specifications
Implementation should be based on Layered Architecture. 
Application should have Presentation, Business and Data Access Layers.
#### 1. Database
Any relational database.

#### 2. Provided Data format
There are 2 csv files in data.zip archive.

##### 2.1 users.csv

Contains users information.

| Name  |  Details|
 ------------- |:-------------:| 
| user_id |   User unique identifier |
| install_date |    Date when user registreted in the system |

##### 2.2 requests.csv

Contains information about users vistits to the system.

| Name  |  Details|
 ------------- |:-------------:| 
| user_id |   User unique identifier |
| request_date |    Date when user has made request to the system |

#### 3. Framework stack
Spring framework,
Struts2
  
#### 4. Api Protocol

##### 4.1 End Points
API should have following end-points
  1. DAU (Daily active users)  
  2. Retention                 
  
##### 4.2 API format
  API should be implemented according to REST rules.
###### 4.2.1 DAU
API accepts list of dates in dd/mm/yyyy format and returns DAUs for that days.
###### 4.2.2 Retention
API accepts two arguments. One is retention type. Accepted values are : "Day1", "Day7", "Day40".
The second one is date in dd/mm/yyyy format. Retention should be calculated starting from that day.
Returns the retention for that day.
