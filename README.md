## Notes about building Ardour5 on FreeBSD

I've already submitted the major patch to the ardour project to #ifdef out the lv2_plugin and uri_map.h
```
./waf configure --also-include=/usr/local/include/ --also-libdir=/usr/local/lib/ --no-phone-home --no-lv2 --cxx11 --use-libc++
```

