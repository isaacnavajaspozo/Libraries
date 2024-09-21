## HTML DOM Parser

### Simple HTML DOM Parser sirve para hacer scraper de una página. Ejemplo:

```php
include('simple_html_dom.php');

$url = 'https://example.com';
$html = file_get_html($url);

// Ejemplo: extraer el título de la página
$title = $html->find('title', 0)->plaintext;

// Devolver como JSON
header('Content-Type: application/json');
echo json_encode(['title' => $title]);

```
