# vulnerable-code

```php
<?php
    $ip = $_GET['ip'];
    system("ping -c 4 " . $ip);
?>
```
