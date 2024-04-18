# vulnerable-code

<p1/> PHP Command vulnerable code <p1/>
    
```php
<?php
    $ip = $_GET['ip'];
    system("ping -c 4 " . $ip);
?>
```
