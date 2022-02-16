# Auth for the Aletheia API

### API Key

To obtain an API key, subscribe to our [Rapid API](https://rapidapi.com/hub) on [https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2](https://rapidapi.com/aletheia-data-aletheia-data-default/api/aletheia2) and follow the instructions.

**Be careful with your API keys. Any abused API Key or wrongly used will be canceled.**

## Authenticating to the API

The Aletheia API expects HTTP Basic Auth with a valid pair of Rapid API keys. Get your `ACCESS_KEYS` from the link above. To authorize your requests, send an HTTP request to one of the API endpoints with the following headers:

```
var axios = require("axios").default;

var options = {
  method: 'GET',
  url: '<ENDPOINT_URL>',
  headers: {
    'x-rapidapi-host': '<API_HOST>',
    'x-rapidapi-key': '<API_KEY>'
  }
};

axios.request(options).then(function (response) {
	console.log(response.data);
}).catch(function (error) {
	console.error(error);
});
```

Note: Node.js is just one of the many laguages available.
