# easyauth

# Challenge

> Can you gain admin access to this site?

> http://easyauth-afee0e67.ctf.bsidessf.net

> * [easyauth.php](easyauth.php)

# Solution

The solution to this challenge is effectively the same trick used in [vhash](../../crypto/vhash/README.md). The user is presented with a login screen, and a test login (guest/guest), and shown the cookie upon successful login. This is the code for the cookie logic from `easyauth.php`.

```
$cookie = 'username=' . $_POST['username'] . '&';
$cookie .= 'date=' . date(DATE_ISO8601) . '&';
setcookie('auth', $cookie);
```

From here, one can simply manually set the cookie to `auth=username%3Dadministrator` and refresh the page. The flag is then revealed as `FLAG:0076ecde2daae415d7e5ccc7db909e7e`.
