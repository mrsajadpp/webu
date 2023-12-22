# Webu.js

[![GitHub license](https://img.shields.io/github/license/mrsajadpp/webu.svg)](https://github.com/mrsajadpp/webu/blob/main/LICENSE)
[![GitHub issues](https://img.shields.io/github/issues/mrsajadpp/webu.svg)](https://github.com/mrsajadpp/webu/issues)
[![GitHub stars](https://img.shields.io/github/stars/mrsajadpp/webu.svg)](https://github.com/mrsajadpp/webu/stargazers)

A web server framework for Node.js.

## Installation

```bash
npm install webu
```

## Usage

```javascript
const Webu = require('webu');

const webu = new Webu();

// Handling GET requests
webu.get('/', (req, res) => {
  res.send(200, '<h1>Hello, World!</h1>', { 'Content-Type': 'text/html' });
});

// Handling PUT requests
webu.put('/update', (req, res) => {
  res.send(200, 'Resource updated successfully!');
});

// Setting a custom error page for 404 errors
webu.error((req, res) => {
  res.send(404, '<h1>Custom 404 Error Page</h1>', { 'Content-Type': 'text/html' });
});

// Setting a custom start message
webu.setStartMessage('Custom message:');

// Starting the server on port 3000
webu.start(3000);
```

## Features

- Simple and lightweight web server framework.
- Support for handling different HTTP methods, including GET and PUT.
- Easily set custom error pages for specific status codes.
- Customize the start message for the server.

## Documentation

### Handling HTTP Methods

Webu.js allows you to handle various HTTP methods such as GET, PUT, POST, DELETE, PATCH, HEAD, OPTIONS, and TRACE.

```javascript
webu.get('/', (req, res) => {
  // Handle GET request for '/'
});

webu.put('/update', (req, res) => {
  // Handle PUT request for '/update'
});

// Similarly, you can use post, delete, patch, head, options, and trace methods
```

### Custom Error Pages

Set custom error pages to handle specific HTTP status codes. In this example, a custom 404 error page is set.

```javascript
webu.error((req, res) => {
  res.send(404, '<h1>Custom 404 Error Page</h1>', { 'Content-Type': 'text/html' });
});
```

### Custom Start Messages

You can customize the start message for your server.

```javascript
webu.setStartMessage('Custom message:');
```

## Contributing

Feel free to contribute by opening issues or submitting pull requests. See [CONTRIBUTING.md](CONTRIBUTING.md) for more information.

## License

This project is licensed under the [ISC License](https://opensource.org/licenses/ISC) - see the [LICENSE](LICENSE) file for details.