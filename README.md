# Ace-creative-academy
## Web Development with Javascript (MongoDB, Express, React, Node)

<!-- Content
* NodeJs
* What is Express
* Setting up a simple server
* HTTP Verbs
* JSON
* Project Idea - Discoy
* Project Breakdown -->


### NodeJs
Node.js is an open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside a web browser. Node.js lets developers use JavaScript to write command line tools and for server-side scripting—running scripts server-side to produce dynamic web page content before the page is sent to the user's web browser.
> [NodeJS Website](https://nodejs.org/), [W3Schools](https://www.w3schools.com/nodejs/default.asp)

#### Setting up a simple server
```javascript
  const http = require('http');

  const hostname = '127.0.0.1';
  const port = 3000;

  const server = http.createServer((req, res) => {
    res.statusCode = 200;
    res.setHeader('Content-Type', 'text/plain');
    res.end('Hello World');
  });

  server.listen(port, hostname, () => {
    console.log(`Server running at http://${hostname}:${port}/`);
  });
```

#### Nodejs Versions and NVM

* [NodeJS Release Versions](https://nodejs.org/en/download/releases/)
* NVM - Node Version Manager is a bash script used to manage multiple released Node.js versions. It allows you to perform operations like install, uninstall, switch version
[Using a Node Version Manager](http://npm.github.io/installation-setup-docs/installing/using-a-node-version-manager.html)

```
nvm -v
nvm ls
nvm use [version]

```

### Express
Express.js, or simply Express, is a minimal and flexible Node.js web application framework, It is designed for building web applications and APIs.

#### Setting up a simple Express server
```javascript
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`Example app listening at http://localhost:${port}`))
```
  
#### Routing & HTTP Verbs
`app.METHOD(PATH, HANDLER)`

```javascript
app.get('/schools', function (req, res) {
  res.send('A GET request to schools')
})
```
```javascript
app.post('/schools', function (req, res) {
  res.send('A POST request to schools')
})
```
```javascript
app.patch('/school', function (req, res) {
  res.send('A PATCH request to schools')
})
```
```javascript
app.delete('/school', function (req, res) {
  res.send('A DELETE request to schools')
})
```

### JSON
JSON (JavaScript Object Notation) is a lightweight data-interchange format.
- [JSON](https://www.w3schools.com/js/js_json_intro.asp)
- [JSON API](https://jsonapi.org/)

```javascript
{
  "type": "articles",
  "id": "1",
  "attributes": {
    "title": "Rails is Omakase"
  },
  "relationships": {
    "author": {
      "links": {
        "self": "/articles/1/relationships/author",
        "related": "/articles/1/author"
      },
      "data": { "type": "people", "id": "9" }
    }
  }
}
```
### Project Idea - Discoy **
### Project Breakdown **
