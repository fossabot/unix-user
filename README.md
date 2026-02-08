# Unix User Utilities
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Falialobidm%2Funix-user.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Falialobidm%2Funix-user?ref=badge_shield)


```
$ npm install unix-user
```

A small set of utilities for managing users in unix systems.

Example:

```javascript
var user = require('unix-user');

user.exists('nick', function(exists) {
	if (!exists) {
		user.create('nick', 'pass', function(err) {
			if (err) {
				return console.log('Error creating user');
			}
			console.log('User created');
		});
	} else {
		user.passwd('nick', 'pass', function(err) {
			if (err) {
				return console.log('Error setting user password');
			}
			console.log('User password updated');
		});
	}
});

```


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Falialobidm%2Funix-user.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Falialobidm%2Funix-user?ref=badge_large)