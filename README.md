# mpdf
Create html page to pdf

##Require in composer.json
```php

{
    "require": {
        "mpdf/mpdf": "^6.1"
    }
}
```

#create a page test.php
```php
require_once __DIR__ . '/vendor/autoload.php';
$html = "<h2>Welcome</h2>";
$mpdf = new mPDF();
$html = mb_convert_encoding($html, 'UTF-8', 'UTF-8');
$mpdf->WriteHTML($html);
$mpdf->Output();
```

browse test.php
