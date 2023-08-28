# Experential-Project

This project is associated with the Northeastern University. As part of the course Integrated Experential Project in the master's curriculum my data sponsor is Docdigitizer. 
The purpose of this project is to produce an interactive dashboard, fed with a month of interaction logs. we neeed to create a dashboard that should provide insights on what are "normal" patterns and flag entries that fall outside that pattern. The analyusis and the model we develop should also be extended to receive a stream of live entries and flag the outsiders on the same way and also alert when heavy load is predicted. 

### Data 

The dataset that we have is the Zip file containing customer request log files in json format of daily logs. 
Each log file contains data on all calls produced during 24 hours in a calendar day. Files for each day are
in separate day folders. Each daily log file has a separate file for every minute that had any logged
activity.
Line Structure: The structure of each line follows below:
- Timestamp
- Source of Envelope
- EventId
- Payload (Json)
  
Payload Structure:
- MessageCode: Same As Source of Envelope, should not vary on your dataset
- EventId: Same as EventId of Line, it is a unique identifier of the message
- EventTime: Moment the event was triggered
- IngestTime: Moment the event was received by the logger
- b64Payload: nested json containing the specific payload based on the message code,

Nested Json Payload:
- RequestId: Sames as EventId of the Line
- SourceIp: The IP address of the API Requester
- HttpMethod: HTTP Method used in the request
- HttpUrl: Url that was requested
- HttpAuth: When present, identifies the API Key that was used to request the URL
- HtppAuthHash: When present, contains the hash of the authorization used
- Resource: When present, contains the Controller method that processed the request
- ResourceClass: When present, contains the Controller Class that processed the request
- ResourceMethod: When present, contains the Controller class method that processed the request
- Organization: key of the organization
- App: when present, contains the key of the application that made the request
- User: when present, contains the key of the user that made the request
- Entity: contains either the key of the app or the user that made the request
- Timestamp_req: moment when the request was received
- Timestamp_resp: moment when the response was returned

## What I have done in the Project:- 

#### Sprint 1: EDA and Data Understanding

- Duration: 3 weeks
- Goals: Understand the dataset, explore trends, and identify key variables for analysis.
- Tasks:
  - Perform initial data quality checks and preprocessing.
  - Conduct EDA to analyze temporal patterns, peak traffic times, and average response times.
  - Visualize data using timelines and graphs to uncover patterns.
  - Identify sources of incoming traffic and their impact.
  - Explore HTTP methods, URLs, authentication, and user details for deeper insights.
  
#### Sprint 2: Predictive Modeling for Traffic Trends

- Duration: 3 weeks
- Goals: Develop predictive models to forecast traffic patterns and optimize resource allocation.
- Tasks:
  - Choose decision trees and random forest classifiers as modeling techniques.
  - Train decision tree classifier on training data and assess accuracy using confusion matrix.
  - Implement random forest classifier to predict HTTP methods for upcoming requests.
  - Achieve 99% accuracy in predicting HTTP methods using the random forest model.
  
#### Sprint 3: Interactive Dashboard Creation

- Duration: 3 weeks
- Goals: Develop interactive dashboards to communicate findings and allow data exploration.
- Tasks:
  - Choose Tableau for dashboard creation.
  - Create Tableau dashboards showcasing daily request counts, hourly distribution, response time, organization breakdown, and HTTP method distribution.
  - Implement filters and dynamic updates for user-driven exploration in Tableau.
  - Develop Python-based dashboards for visualizing traffic patterns and trends.

#### Review and Adaptation:

- Duration: 1 week
- Goals: Review project outcomes, assess achieved goals, and plan for next steps.
- Tasks:
  - Evaluate the success of the project's goals and tasks in each sprint.
  - Gather feedback from stakeholders on the generated insights, predictions, and dashboards.
  - Identify areas of improvement and lessons learned for future projects.
  - Plan for any further iterations or enhancements based on feedback.

#### Key Achievements:

- Deepened understanding of server traffic behavior through EDA techniques.
- Uncovered patterns and trends using visualizations and graphs.
- Predicted future traffic trends with high accuracy using decision trees and random forests.
- Created interactive dashboards for stakeholders to explore insights and trends.
- Optimized resource allocation based on traffic patterns and predictions.

