# ITC303 CodePulse Deliverables

The following are requirements laid out for delivery of ITC303 Software engineering project being developed by CodePulse at Charles Sturt University during 2024. Anomaly is working with:

- @dnavarroau
- @elliotmitchum
- @Sam-WebP

to deliver an initial reboot of [RFC-002](RFC-002) with boundaries to make it feasible to deliver a working v1 during the academic term.

The deliverable is required to fit into the larger vision of the project.

## Functional requirements

The following minimum set of requirements are delivered based on the following assumptions:

- A property file export is loaded using the Django [initial data load](https://docs.djangoproject.com/en/5.0/howto/initial-data/) utilities. The models should allow for versioning of the property data
- Payments are not live

### Certificate ordering

At a minimum the user is able to place an anonymous order for certifiates, this includes:

- The user is able to find the land parcel using `Lot`, `Section`, and `Plan` numbers
- The user is able to select one or more certificates to order
- The user is able to enter their deliver details (for electronic delivery)
- The user is able to pay for the order using a credit card
- The user is presented with a confirmation page upon successful payment

### Fulfilment workflow

- The council is able to view orders
- The council is able to filter the orders by status
- The council is able to upload documents against an order
- The council is able to mark an order as fulfilled
- The council is able to leave notes against an order

Additionally:

- Upon uploading a file an email notification is sent to the user that placed the order

### Nice to haves

- Customers of the council are able to see history of their orders
- Customers are able to link their cards for future use
- Council users are able to generate a PDF for filing in their document management system.
- Users are able to upload new data files for property data

## Technical deliverables

- Containerised Django application written using the standard Django stack and any plugins
- Authentication to be restricted to local user accounts. Social logins etc are not expected
- Documentation to support installation and deployment of the software
- Stripe integration to use a test account
- A working deployment of the software on a cloud provider

For the purposes of this project we do not expect deployment in Kubernetes, a simple `docker compose` based deployment will be sufficient.

## Conventional requirements

Anomaly uses the following habitual conventions to ensure standards across team members:

- [Convention for commit messages](https://www.conventionalcommits.org/en/v1.0.0/) for `git` commit message
- [PEP8](https://www.python.org/dev/peps/pep-0008/) using plugins for Visual Studio code
- [Docker best practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/) for filenames and directives such as `LABELS`
