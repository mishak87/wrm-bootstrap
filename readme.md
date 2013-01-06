Bootstrap for Nette projects using Web Resource Management
==========================================================

This is still experimental and I am working on way to circumvent composer definition and manual including of config.

## Instalation

### Composer

Add to `composer.json` requirement `"twitter/bootstrap": "2.2.2"` and add `twitter/bootstrap` to repositories:

```json
"repositories": [
	{
		"type": "package",
		"package": {
			"version": "2.2.2",
			"name": "twitter/bootstrap",
			"source": {
				"url": "https://github.com/twitter/bootstrap.git",
				"type": "git",
				"reference": "tags/v2.2.2"
			},
			"dist": {
				"url": "https://github.com/twitter/bootstrap/zipball/v2.2.2",
				"type": "zip"
			}
		}
	}
]
```

### App config

```yaml
includes:
	- ../../libs/mishak/wrm-bootstrap/config.neon

parameters:
	libsDir: %appDir%/../..
```
