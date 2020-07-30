## Microservices

#### The general idea:
* monolith architecture: make one GET request to the posts db, and another GET request to the comments db every time we want to view all posts and comments
* microservices: every time a post or comment is created, it is automatically linked together and stored in a third query service asynchronously. when we need to view the entire posts/comments list, we make ONE GET request to the query service. <br> upside: 0 dependencies and very fast. even if the posts or comments service is down, the query service already has data to send. <br> downsides: data duplication and harder to engineer.

Even if I killed my comments and post service both, my web page is serving up data to the user just fine!