# Teamwork V (Project Requirements Specification)
## Team members
Tony Thesslund / e2101348

## Problems
The objective of this teamwork assignment is to identify, structure, and prioritise the requirements for the project application. The team should develop a clear understanding of what the application needs to accomplish, who will use it, and what technical and quality characteristics it must fulfill.

## 1. Identify the Stakeholders and User Needs

Start by identifying the main stakeholders and potential users of the application. Consider their different needs, expectations, and responsibilities.

### Stakeholders
#### Hotel owners
- Needs: Working software solution

- Expectations: Working software solution

- Responsibilities: Together with own IT team, cooperate with the development team. Attend meetings to see progress, give feedback.

#### System administrators
- Needs: Working software solution. Training.

- Expectations: Secure, stable and easy to maintain system.

- Responsibilities: Understanding the software. Manage user accouts and permisions. Feedback.

#### Hotel staff
- Needs: Intuitive application. Easy to find/modify the needed information. Training.

- Expectations: Intuitive application. Easy to find/modify the needed information.

- Responsibilities: Learning how to use the application. Give feedback for the software


#### Customers
- Needs: Ability to view, book and pay for available rooms.

- Expectations: Intuitive and responsive UI. Easy to book and pay.

#### Development team
- Needs: Clear requirements and feedback
- Expectations: Communication and feedback from other stakeholders
- Responsibilities: Design, develop, test and maintain application.


## 2. Define the Overall Application Requirements

Develop a set of requirements for the application as a whole. The requirements should describe what the application must do and the qualities it must have. Consider, for example:

### Functional requirements
*What functions and services must the application provide?*
- User authentication and authorization
- User interface: Both internal room management and for the customer
- Data management: Store booking / room availability / customer data.
- Search functionality: Hotel staff need to be able to search based on customer or room number.
- Payment processing

### Performance requirement
*How quickly and efficiently should the application operate?*

The application should work seamlessly

### Usability requirements
*How easy should the application be to learn and use?*

On the customer side, there should be no barrier of entry. The staff should be able to use its features after some training.

### Reliability and availability
*How reliable should the application be, and how should it behave in case of failures?*

The application should be available at all times. In case of failures, the recovery time should be short.

### Security
*What data and operations need to be protected?*

Customer data and payment processing needs to be secure.

### Maintainability
*How easy should the application be to maintain, modify, and extend?*

Should be easy to deploy for multiple hotels, for example.

### Compatibility and integration
*What other systems, platforms, or services should the application interact with?*

- Payment processors
- (External booking providers)

### Constraints
*Are there standards, legislation, organisational requirements, or technical limitations that need to be considered?*

- GDPR + Tietosuojalaki
- Budget restraints

## 3. Partition the application into logical subsystems
Divide the application into logical subsystems or major components. The decomposition should make it easier to understand the responsibilities of each part of the system and how the parts interact.

For each subsystem:
- Define its main purpose and responsibilities
- Define the inputs and outputs
- Define specific functional and non-functional requirements

### Front-End, Customer UI (webapp)
Provides the user interface for the customer. 
Customer is able to view available rooms and book them.

Inputs:
- Customer data
- Booking data
- Room data
- Room availability
- Payment information

Outputs:
- Customer data
- Booking data
- Payment data

#### Requirements
- Needs provide the customer with a browser UI that works on a majority of devices and browsers.
- UI/UX should be intuitive
- Integration with payment processors
- Search functionality
- Should reliably display available rooms
- Allow customers to book rooms
- Provide clear confirmation after successful booking and payment
- Payment information has to be handled securely

### Front-End, Management UI (webapp)
The management UI should provide the ability to view room availability and bookings. It should also allow for modifying bookings.

Inputs:
- Customer data
- Booking data
- Room data
- Room availability

Outputs:
- Modified Room/Booking data

#### Requirements
- Should be intuitive, easy to use
- Reliably reads and writes customer, booking and room data
- Should allow staff to create, modify and cancel bookings
- Should allow staff to update room information
- Provide appropriate access depending user roles
- Display current and upcoming bookings

### Back-End, Logic
Connection between the Front-End and the database. Handles business logic of the application.

Inputs:
- Customer data
- Booking data
- Room data
- Requests from front-end
- Payment information

Outputs:
- Customer data
- Booking data
- Room availability
- Booking confirmations
- Payment status
- Error messages

#### Requirements
- Should reliably process requests from both customer and management UI
- Validate incoming data
- Securely handle customer data
- Communicate with payment processor
- Handle booking creation, modification and cancellation
- Provide useful error messages

### Database
Stores room, booking and customer data

Biggest concern here is keeping customer data secure.

Inputs: 
- Customer data
- Booking data
- Room data
- Payment information

Outputs:
- Customer data
- Booking data
- Room availability
- Room information

#### Requirements
- Should reliably store and retrieve data
- Customer data MUST be protected from unauthorized access
- Regular backups

### Infrastructure
Servers, networking, storage.

Inputs:
- Application software
- Database
- User requests
- External service requests

Outputs:
- Running web application
- Network access
- Application and database availability

## 4. Using Quality Function Deployment
Use Quality Function Deployment (QFD) to analyse the relationship between stakeholder/customer needs and the technical requirements of the application. The analysis should:

- Identify the most important customer/user needs
- Translate these needs into measurable technical or system requirements
- Prioritize the requirements based on their importance to stakeholders and the project.