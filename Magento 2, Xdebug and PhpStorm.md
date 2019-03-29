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
