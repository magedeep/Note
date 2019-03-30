This tutorial is about:
- How to config Phpstorm to work with Xdebug
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

Add Configuration > Add New Configuration > PHP Web Page 

![phpstorm_config](https://user-images.githubusercontent.com/5145257/55270197-c5654600-52ce-11e9-9e52-9d65d32ea517.png)

> Create Server 
![Screenshot from 2019-03-30 09-35-32](https://user-images.githubusercontent.com/5145257/55270240-3a388000-52cf-11e9-8a5b-e6fa404fd4c0.png)

That is done for configuration Xdebug and Phpstorm. Next step how to set breakpoints and debug Magento 2
