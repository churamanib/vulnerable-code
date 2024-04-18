# vulnerable-code

<h1/> PHP Command vulnerable code <h1/>
    
```php
<?php
    $ip = $_GET['ip'];
    system("ping -c 4 " . $ip);
?>
```
