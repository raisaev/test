# Woocommerce Plugin

Integration with Wordpress woocommerce plugin

## Skip SSL validation

### Register hook in `M2e_SC_Bootstrap::run`
```php
$facade->add_action( 'http_api_curl', function ( $curl ) {
    curl_setopt( $curl, CURLOPT_SSL_VERIFYHOST, 0 );
    curl_setopt( $curl, CURLOPT_SSL_VERIFYPEER, 0 );
} );
```