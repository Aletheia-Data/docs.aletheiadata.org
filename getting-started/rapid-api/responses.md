# Public Rest API for Aletheia

### General API Information

* The root API URL is [https://aletheia2.p.rapidapi.com/](https://aletheia2.p.rapidapi.com/) (as we use the Rapid API service to distribute our API)
* Parameters for GET requests must be sent as a `query string`.
* All other request methods require parameters in the request body as `Content-Type: application/json`
* Parameter order does not matter.
* All timestamps are in milliseconds.
* API errors and results take the following form:

```
{
  "code": "ALETHEIA_API_ERROR_CODE",
  "body": "Error message appears here."
}
```

### Rate limiting

If your account repeatedly gets rate limited, then you are using the API improperly and must back off. Failure to do so will cause your account to lose API access. Aletheia retains the right to ban your account with no notice if you are abusing the API.

The rate limits are set generously and are not meant to prohibit any amount of normal usage. In the future, we will standardize our rate limits and provide more explicit feedback about how many remaining requests you can send each minute.

###

###

\
