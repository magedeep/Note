Install magento 2 using command line

```sh
php setup:install --<option>=<value> ... --<option>=<value>
```
Reference magento doc
https://devdocs.magento.com/guides/v2.3/install-gde/install/cli/install-cli-install.html

Example:
```sh
php bin/magento setup:install --base-url=http://m2.local --backend-frontname=admin --db-host=localhost --db-name=m2 --db-user=admin --db-password=123456 --admin-firstname=bang --admin-lastname=nd --admin-email=myemail@gmail.com --admin-user=admin --admin-password=123456a --language=en_US --currency=USD --timezone=America/Chicago
```
