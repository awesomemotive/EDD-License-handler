EDD License Handler
===================

License / updater handler for Easy Digital Downloads extensions.

This class should be included with all premium EDD extensions sold through EasyDigitalDownloads.com in order to include licensing and updates.

**Make sure you place both the `EDD_License_Handler.php` class and the `EDD_SL_Plugin_Updater.php` class in the same location.**

```php
// Load the EDD license handler only if not already loaded. Must be placed in the main plugin file
if( ! class_exists( 'EDD_License' ) )
	include( dirname( __FILE__ ) . '/includes/EDD_License_Handler.php' );


// Instantiate the licensing / updater. Must be placed in the main plugin file
$license = new EDD_License( __FILE__, 'Extension Name Here', '1.0', 'Your Name' );
```

Full Example:
=============
```php

// Load the EDD license handler only if not already loaded. Must be placed in the main plugin file
if( ! class_exists( 'EDD_License' ) )
	include( dirname( __FILE__ ) . '/includes/EDD_License_Handler.php' );

$license = new EDD_License( __FILE__, 'PDF Stamper', '1.0.5', 'Daniel J Griffiths' );
```

Requirements
============

This class can only be used with EDD v1.7 and later.
