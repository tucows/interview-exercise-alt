# interview-exercise

Tucows Interview Exercise

## Instructions

- Please create a repo in which you will attempt the exercise.
- When you are done share repo link with HR
- In a file called setup.md please include instructions on how to run and test you application
- Please use GO for your solutions
- Partial solutions are accepted, however do your best to complete as much as posible in allocated time period
- Any partial solution should
  *  still be functional
  *  include a decription on how would the missing part/s be designed given you had more time

## Tasks

Provide simple order processing system for an arbitrary product of your choice. The system should include

- Web microservice for order management (just HTTP API, no web forms)
- Postgres database
- Another microservice for payment processing
- Some sort of messaging broker for asynchronous communication between two microservices

### Order Management Microservice

Service must have but not limited to

- Predefined single customer (with option to support multiple in future)
- Predefined single product (with option to support multiple in future)
- Ability to submit an order for specified customer and product. Order should include all relevant information.
- Ability to retrieve previously submitted order

As part of order creation service must submit an asynchronous request to payment microservice with all relevant data. Result of payment request should be reflected in order status. 

### Payment Processing Microservice

Service must have but not limited to 

- Ability to receive and handle requests from order management service
- Processing of payment can be simulated (amount <= 1000 = success, amount > 1000 = failure)
- Ability to notify order management service regarding payment result


## Additional requirements

- Provide unit tests
- Provide any documentation you think might be helpful
- Feel free to add anything that you think might be useful

