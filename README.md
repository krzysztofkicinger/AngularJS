# AngularJS

Project main purpose is to provide base template for AngularJS, Twitter Bootstrap, Java Script Application

### Installation

##### Node.js Server

First of all, you have to install Node.js for particular OS:

```http
https://nodejs.org/download/
```

(You can skip this step if you want to use nodejsserver/start.js script)
Next, you need to download modules required for server initialization:

```sh
npm install connect
npm install serve-static
npm install http
```

**Note**:
serve-static module is required if you are going to use connect module from 3.X.X version (if version 2.X.X is used, serve-static module is not required)

##### AngularJS and Twitter Bootstrap

AngularJS 1.3.14 and Twitter Bootstrap 3.3.2 are delivered with the project distribution. If you want to change version of used libraries please download releases from:

```http
https://angularjs.org/
http://getbootstrap.com/getting-started/#download
```

### Initialization

First of all, you need to start node.js server. In order to do it, please go to nodejsserver, start command line prompt and enter:

```sh
node start.js
```

### Test correctness

Open webbrowser and enter URL:

```http
http://localhost:5000/
```

If everything was configured successfully, the html page should be returned.
