# aws_ses
Complete solution in Java for sending emails using SES

Aim of this project is to create a layer on top of AWS SES API, that will:
- pick up the SES configuration from a file
- send email
- check status of the delivery
- do necessary follow-up action such as retry
- provide a way to configure the follow-up action

Some follow-up actions
- retry using the same port
- retry using a different port
- retry with a different credential
- retry with a different region (and credential)
- etc

Some configuration options
- retry after how long (for example, to avoid being throttled)
- max time to be spent on a message
- failure records to go to what DB - the particulars of the DB

In short, explore all aspects of the API and pull up all ways to explode the scenarios and bring them under configuration. This project will tend to blow up in complexity, but keep interfaces simple to use.

