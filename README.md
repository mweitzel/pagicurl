## pagicurl

Wraps curl with some bash to attempt automaitc pagination.

Uses the Link Header as defined here: http://tools.ietf.org/html/rfc5988#section-5

Only works with json response types

Works just like curl, but requires uri to come first.


Calling this:
```bash
$ ./pagicurl https://api.github.com/user/repos -H "Authorization: token $GITHUB_API_TOKEN"
```
will return a json array of all repositories

where this:
```bash
$ curl https://api.github.com/user/repos -H "Authorization: token $GITHUB_API_TOKEN"
```
would only return 30, or whatever the default pagination limit is
