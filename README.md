# Cmarty template engine
Cmarty is a template engine for PHP like Smarty, facilitating the separation of presentation (HTML/CSS) from application logic. 


## Requirements
Cmarty can be run with PHP 7.1 to PHP 8.1.

## Installation
Cmarty versions 1.0 or later can be installed with [Composer](https://getcomposer.org/).

To get the latest stable version of Cmarty use:
```bash
composer require phplight/cmarty
````


## Example

Cmarty can convert tpl file from tpl to php. You can pm/email for code details.

```php
$writer = new Cmarty();
$data = array(
    'id' => $this->id,
    'block_id' => $this->block_id,
    'theme' => $this->theme,
    'folder' => $this->folder,
    'file' => $this->tpl,
);

$tpl = $writer->getDestinationFromBlock($data, 'tpl');
$php = $writer->getDestinationFromBlock($data, 'php');
$writer->save($tpl, $php);
````