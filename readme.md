
# Compro behat

Compro behat is blank behat project built on the [Behat Drupal Extension](https://github.com/jhedstrom/drupalextension).

## Requirements

- PHP **5.3.5+** with the following libraries:
  - curl
  - mbstring
  - xml
- Composer
- cURL
- Docker & [docker-selenium](https://github.com/SeleniumHQ/docker-selenium) (optional)

## Installation

```
composer install
```

### Optional but recommended
Grab and run the standalone Firefox selenium container with debugging capabilities (VNC).

```
docker pull selenium/standalone-firefox-debug
docker run -d -p 4444:4444 -p 5900:5900 selenium/standalone-firefox-debug
```

This will forward the ports so you can access Selenium on port 4444 and VNC on port 5900.
These ports can be changed if you wish to have multiple containers running.

## Configuration

Configuration can be found in the behat.yml file. The base_url is set to the default
Vagrant URL for compro work. A files directory exists with a test.pdf file for testing file uploads.
Any files needed for testing can be placed in the directory.
