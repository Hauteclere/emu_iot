# To Do:

- add lambda to push to dynamodb before returning parsed data
- clean up extra stuff:
  - UserName='db_user'
  - PolicyName='db_user_policy'
- check lambda functions don't need to deal with batches better - right now they probably just accept a single message at a time which will get expensive when lots and lots of messages are landing
- set expiry period on s3
- update authentication system for local analysis from access keys to something more secure?
- add logging
- set up secure secrets?