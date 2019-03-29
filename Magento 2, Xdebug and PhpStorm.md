This is tutorial about:
- How to config Phpstorm working with Xdebug
- how to set breakpoints and debug Magento 2

I am using LEMP stack.
In xdebug.ini add new line to end file

```
xdebug.remote_enable = 1
xdebug.remote_port = 9001
xdebug.show_error_trace = 1
```
In PhpStorm access to Settings > Languages & Frameworks > PHP > Debug and set port
![xdebug_config_port](https://user-images.githubusercontent.com/5145257/55206690-f9c2fe80-5209-11e9-8378-c68583b64d0c.png)
