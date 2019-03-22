# How to log all sql queries

In your app/etc/di.xml, replace the line:
```
<preference for="Magento\Framework\DB\LoggerInterface" type="Magento\Framework\DB\Logger\LoggerProxy"/>
```
To
```
<preference for="Magento\Framework\DB\LoggerInterface" type="Magento\Framework\DB\Logger\File"/>
```

And change
```
<type name="Magento\Framework\DB\Logger\LoggerProxy">
    <arguments>
        <argument name="loggerAlias" xsi:type="init_parameter">Magento\Framework\Config\ConfigOptionsListConstants::CONFIG_PATH_DB_LOGGER_OUTPUT</argument>
        <argument name="logAllQueries" xsi:type="init_parameter">Magento\Framework\Config\ConfigOptionsListConstants::CONFIG_PATH_DB_LOGGER_LOG_EVERYTHING</argument>
        <argument name="logQueryTime" xsi:type="init_parameter">Magento\Framework\Config\ConfigOptionsListConstants::CONFIG_PATH_DB_LOGGER_QUERY_TIME_THRESHOLD</argument>
        <argument name="logCallStack" xsi:type="init_parameter">Magento\Framework\Config\ConfigOptionsListConstants::CONFIG_PATH_DB_LOGGER_INCLUDE_STACKTRACE</argument>
    </arguments>
</type>
```
To
```
<type name="Magento\Framework\DB\Logger\File">
    <arguments>
        <argument name="logAllQueries" xsi:type="boolean">true</argument>
        <argument name="debugFile" xsi:type="string">debug/sql.log</argument>
    </arguments>
</type>
```
