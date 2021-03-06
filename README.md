# TimeAgoBundle
Provides a simple twig filter for expressing time difference in words for Symfony. 
Uses a range of +-7 days, after that, the actual date is returned.

## Install
Composer (<a href="https://packagist.org/packages/eschmar/time-ago-bundle" target="_blank">Packagist</a>):
```sh
composer require eschmar/time-ago-bundle ^v2.0.0 # Symfony ^5.0
```

or for older symfony versions:
```sh
composer require eschmar/time-ago-bundle ^v1.1.0 # Symfony ^4.x
composer require eschmar/time-ago-bundle ~v0.4.0 # Symfony ^2.8
composer require eschmar/time-ago-bundle ~v0.5.0 # Symfony ^3.4
```

app/Appkernel.php (Symfony <4):
```php
new Eschmar\TimeAgoBundle\EschmarTimeAgoBundle(),
```

## Usage
```twig
{{ date('now')|ago }}
{# just now #}

{{ date('now').modify('-3 minutes')|ago }}
{# 3 minutes ago #}

{{ date('now').modify('-3 months')|ago('r') }}
{# actual date in 'r' format #}

{{ date('now').modify('+4 hours')|ago('r') }}
{# in 4 hours #}
```

Change [default format](http://php.net/manual/en/function.date.php) in `config.yml`:

```yml
eschmar_time_ago:
    format: 'Y-m-d H:i:s'
```

# Translations available

* Belarusian
* Croatian
* Czech
* Danish
* Dutch
* English
* French
* Finnish
* German
* Hindi
* Hungarian
* Indonesian
* Italian
* Malay
* Norwegian
* Polish
* Portuguese (Brazil)
* Romanian
* Russian
* Slovenian
* Spanish
* Swedish
* Tagalog
* Turkish
* Ukranian
* Vietnamese

# License
MIT License
