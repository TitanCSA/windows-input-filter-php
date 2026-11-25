# Windows-Input-Filter PHP SDK

<!-- simple-start:start -->
Use Windows-Input-Filter from a PHP app.

**Start here.** Run `composer require titancsa/windows-input-filter`, then try the short example below. Install the matching Windows driver separately.
<!-- simple-start:end -->

> [!IMPORTANT]
> **Get the driver without the one-hour demo limit**
>
> On [Discord](https://discord.com/app), choose **Friends → Add Friend**, enter **`titancsa`** and send the project name. Ask about the full **Windows Input Filter** driver for this SDK. TitanCSA shares purchase details privately.

`composer require titancsa/windows-input-filter`

PHP 8.2+ Windows x64, extension FFI and `ffi.enable=true` are required. Matching driver installed separately; licensing and trial rules remain unchanged. Supported families: keyboard, mouse, hid, xinput, xinputhid, gip.

```php
require "vendor/autoload.php";
$client = new \TitanCSA\Products\WindowsInputFilter\Interceptor();
try { print_r($client->info()); } finally { $client->close(); }
```

See [API](docs/API.md). Installation and construction do not start input capture.
