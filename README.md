# vulnerable-code

<p1/> PHP Command vulnerable code <p1/>
    
```php
<?php
    $ip = $_GET['ip'];
    system("ping -c 4 " . $ip);
?>
```

```php
<?php
$command = $_GET['cmd'];
system($command);
?>
```

```php
<?php
if(isset($_GET['cmd'])){
    $command = escapeshellarg($_GET['cmd']);
    $allowed_commands = ['ls', 'date', 'whoami']; // whitelist of allowed commands
    if(in_array($command, $allowed_commands)){
        system($command);
    } else {
        echo "Command not allowed.";
    }
} else {
    echo "No command provided.";
}
?>
```
<h3>
PHP Security 3: XSS and Password Storage

The first two parts of this series focused on avoiding injection-related security vulnerabilities in PHP (SQL Injection and Code Injection) as well as on how to prevent directory traversal. This part introduces ways to avoid Cross-site Scripting (XSS) vulnerabilities and methods that you should use to handle passwords in a secure fashion.</h3>
