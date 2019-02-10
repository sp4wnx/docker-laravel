# Docker Laravel

That's my solution to work with Docker and Laravel using the minimum resources possible to be as lighter as possible.

As I had problems to make this work because to connect on MySQL container was easy, but then when the PHP container needed to use Guzzle for example, then was getting ***'cURL error 7'***.

The best solution I found was create a network and use alias in the application to connect to the correct container.

**Example:**
  In my **.env** file (**Laravel Project**) I'm using the aliases ***'docker-alias-db-mysql'*** and ***'docker-alias-webserver'***, obviously you can use whatever you want. I've used the prefix 'docker' to be easier to remember whenever I look back to the code.

  - DB_HOST=docker-db-mysql
  - PASSPORT_LOGIN_ENDPOINT=http://docker-webserver/oauth/token
