 [https://doc.sun-panel.top/](https://doc.sun-panel.top/)

[https://doc.sun-panel.top/zh_cn](https://doc.sun-panel.top/zh_cn/introduce/project.html)

[https://github.com/hslr-s/sun-panel](https://github.com/hslr-s/sun-panel)



[https://hub.docker.com/r/hslr/sun-panel](https://hub.docker.com/r/hslr/sun-panel)



[https://github.com/hslr-s/sun-panel/blob/master/public/logo.png](https://github.com/hslr-s/sun-panel/blob/master/public/logo.png)

## <font style="color:rgb(60, 60, 67);">docker-compose</font>
```shell
version: "3.2"

services:
  sun-panel:
    image: "hslr/sun-panel:latest"
    container_name: sun-panel
    volumes:
      - ./conf:/app/conf
      - /var/run/docker.sock:/var/run/docker.sock # Mount the Docker socket
      # - ./runtime:/app/runtime # Mount the log directory
      # - /mnt/sata1-1:/os # Mount the hard drive (modify according to your needs)
    ports:
      - 3002:3002
    restart: always
```

