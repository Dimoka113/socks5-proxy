# Socks5-Proxy

A minimal [SOCKS5](https://tools.ietf.org/html/rfc1928) proxy written in C.

## Build

We use CMake to build this project.

```sh
mkdir -p build && cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
make -j
```

If you don't have CMake installed, you could build it with GCC.

```sh
gcc proxypass.c -o proxy -pthread -O3
```

## Run

Run a SOCKS5 proxy on port 1080.

```sh
./proxy -p 1080
```
also you can add username and password your proxy server with:
```sh
./proxy -p 1080 --username test --password yourpassword
```

Test it with `curl`.

```sh
curl --socks5 127.0.0.1:1080 https://www.baidu.com
```

You may also set the proxy in your browser as SOCKS5 on 127.0.0.1:1080, and start browsing websites.

For more information, run `./proxy -h` for help.

## Использование в ([Pterodactyl](https://pterodactyl.io/))

Install Egg from [here](https://promo.i113d.ru/socks5proxy/proxy.zip)

Add Egg in your panel ([how](https://promo.i113d.ru/socks5proxy/installeggs.mp4)?)

Enjoy!




