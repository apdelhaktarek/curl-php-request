# curl-php-request
PHP cURL GET request and request's body
### Requirements

PHP Curl Class works with PHP 7.0, 7.1, 7.2, 7.3, 7.4, 8.0, and 8.1.

### Quick Start and Examples

```php
require_once( dirname(__FILE__) . '/HTTPRequester.php' );

$target_url = "http://localhost/upload";
$fname = 'D:\1.MP4';
$cfile = new CURLFile(realpath($fname));
$data = array(
    'file' => $cfile
);

$header = array(
    'Content-Type: multipart/form-data'
);

$result = (HTTPRequester::HTTPPost($target_url, $data, $header, false));

if ($result === FALSE) {
    echo "Error sending" . $fname;
} else {
    echo "Result: " . $result;
}

```
