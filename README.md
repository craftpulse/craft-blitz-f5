<p align="center"><img width="130" src="https://github.com/putyourlightson/craft-blitz-f5/assets/57572400/1441dcf1-96a5-4bf8-80d3-25ed796983fd"></p>

# Blitz F5 Purger for Craft CMS

The F5 Purger plugin allows the [Blitz](https://putyourlightson.com/plugins/blitz) plugin for [Craft CMS](https://craftcms.com/) to purge pages cached on F5’s Edge CDN.

## License

This plugin is licensed for free under the MIT License.

## Requirements

This plugin requires [Craft CMS](https://craftcms.com/) 5.0.0 or later.

## Usage

Once installed, the F5 Purger can be selected in the Blitz plugin settings or in `config/blitz.php`.

```php
// The purger type to use.
'cachePurgerType' => 'putyourlightson\blitzf5\F5Purger',

```

Note that when purging multiple cached pages, only a single URI with a wildcard character after the longest common prefix is sent. This helps reduce the number of API requests made to the F5 CDN.

For example, if the URIs are:

- `/foo/bar`
- `/foo/qux/baz`

Then only a single API request will be sent with the URI pattern `/foo/*`.

---

Created by [PutYourLightsOn](https://putyourlightson.com/).
