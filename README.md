## pagicurl

Curl paginated results. This script wraps curl and follows pagination headers for succesive calls.

Uses the Link Header as defined here: http://tools.ietf.org/html/rfc5988#section-5

Only works with json response types

Works just like curl, and accepts all flags, but requires uri to come first.

Calling this:
```bash
$ ./pagicurl https://api.github.com/user/repos -H "Authorization: token $GITHUB_API_TOKEN"
```
will return a json array of all repositories

where this:
```bash
$ curl https://api.github.com/user/repos -H "Authorization: token $GITHUB_API_TOKEN"
```
would only return up to the first 30 results
