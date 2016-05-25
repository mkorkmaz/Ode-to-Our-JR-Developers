
# Ode to Our JR PHP Developers
## Self-service Code Review and Fix Before Commit & Push The Changes

### What you need?

Although this document mentions about Mac OSX, all tools should be installed easily for the other operating systems.


For Mac OSX,  all these packages mentioned below can be installed using [Homebrew](http://brew.sh/). If you don't have Homebrew you can install Homebrew as follows:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```


##[PHP Mess Detector](https://phpmd.org/)

PHPMD "takes a given PHP source code base and look for several potential problems within that source".

### Installation
```
brew install homebrew/php/phpmd
```

### Example configuration
```
<?xml version="1.0" encoding="UTF-8"?>
<ruleset name="pcsg-generated-ruleset" 
    xmlns="http://pmd.sf.net/ruleset/1.0.0" 
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
    xsi:schemaLocation="http://pmd.sf.net/ruleset/1.0.0 http://pmd.sf.net/ruleset_xml_schema.xsd"
    xsi:noNamespaceSchemaLocation="http://pmd.sf.net/ruleset_xml_schema.xsd">
<description>Created with the PHP Coding Standard Generator. http://edorian.github.com/php-coding-standard-generator/
</description>
<rule ref="rulesets/codesize.xml"/>
<rule ref="rulesets/controversial.xml"/>
<rule ref="rulesets/design.xml"/>
<rule ref="rulesets/naming.xml"/>
<rule ref="rulesets/unusedcode.xml"/>
</ruleset>
```

You can generate a config at [PHP Coding Standard Generator](http://edorian.github.io/php-coding-standard-generator/#phpmd)

### Usage
```
phpmd /path/to/code html ~/phpmd.xml --reportfile ~/Desktop/report.html
```

## [PHP Code Sniffer, Beautifier and Fixer](https://github.com/squizlabs/PHP_CodeSniffer)

PHPCS "tokenizes PHP files and detects violations of a defined set of coding standards". 
PHPCBF beautifies and fixes codes automatically.

### Installation of both tools
```
brew install php-code-sniffer

```
### Code sniffer usage
```
phpcs /path/to/code
```

### Code fixing usage
```
phpcbf /path/to/code
```


## [PHP Copy/Paste Detector](https://github.com/sebastianbergmann/phpcpd)
PHPCPD is a Copy/Paste Detector (CPD) for PHP code

### Installation
```
brew install homebrew/php/phpcpd
```
### Usage
```
phpcbf /path/to/code
```