# Configure your Wordpress files

Add your Wordpress files into this folder and they will be used instead of the default Wordpress original source.

## HTTPS

Configure Wordpress to inform it is running behind a proxy server and using HTTPS. Add to your `wp-config.php` the following lines:

```php
define('FORCE_SSL_ADMIN', true);

if (strpos($_SERVER['HTTP_X_FORWARDED_PROTO'], 'https') !== false)
       $_SERVER['HTTPS']='on';
```

For more information visit [http://codex.wordpress.org/Administration_Over_SSL#Using_a_Reverse_Proxy](http://codex.wordpress.org/Administration_Over_SSL#Using_a_Reverse_Proxy).
