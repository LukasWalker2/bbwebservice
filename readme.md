# bbwebservice

`bbwebservice` is a small python library to make simple webserver.

## installation

to install this library use the pip command: `pip install bbwebservice`

## usage

import:

```py
from bbwebservice.webserver import * 
```

```py
@register(route='/', type= MIME_TYPE.HTML)
def main_page():
    return load_file('/content/index.html')
```


## server configuration:
In the directory `/config`, there is a file named `config.json`. Here can config

```json
{
    "ip": "localhost",
    "port": 5000,
    "queue_size": 10,
	"SSL": false,
	"cert_path" : "",
	"key_path" : ""
}
```

If you intend to keep the application centrally (online), it is recommended to set the value of `ip` to either `default` or the IP address of the respective server. Additionally, it is advisable to activate `SSL` and set the corresponding paths for `cert_path` and `key_path`. 

### Recommended Ports

- 5000: For testing purposes
- 443: For HTTP (SSL = false)
- 80: For HTTP (SSL = false)

![example charts](charts-example.png)