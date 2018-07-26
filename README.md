EDD License Handler
===================

The `EDD_License` class is included in Easy Digital Downloads core and should not be included in any integration for Easy Digital Downloads.

Who is this for?
===================
The use of this example is intended for extensions that integrate _with_ Easy Digital Downloads, being sold on stores using Easy Digital Downloads _and_ the Software Licensing extension, so that they can display a license key field within the Easy Digital Downloads settings.

Registering your EDD Extension with the License Handler:
========================
If you have an extension for Easy Digital Downloads, that you wish to have your license key field show in the `Downloads > Settings > Licenses` list, use the following to register your Extension with the License Handler.
```php

// Easy Digital Downloads includes the licnese handler class already, you do not need to include it.

/*
 * Parameters to send to the license handler
 *
 * $plugin_file     - The main plugin file name being registered
 * $product_name    - The name of the Downlaod on the store (exact match)
 * $product_version - The version of the plugin
 * $author_name     - The author name for the plugin
 * $item_id         - This is the post_id of the Download
 * $store_url       - The store URL where this product should check for updates
 *
 */
// $license = new EDD_License( $plugin_file, $product_name, $product_version, $author_name, $item_id, $store_url
if ( class_exists( 'EDD_License' ) ) {
    $license = new EDD_License( __FILE__, 'Product Name', '1.0.0', 'Author Name', 1, 'http://example.org' );
}
```

Requirements
============

This class can only be used with EDD v1.7 and later.