## Notes about building Ardour5 on FreeBSD

I've already submitted the major patch to the ardour project to #ifdef out the lv2_plugin and uri_map.h
```
./waf configure --also-include=/usr/local/include/ --also-libdir=/usr/local/lib/ --no-phone-home --no-lv2 --cxx11 --use-libc++
```

Alternatively, if we are going to use lv2, we need to update the wscript with the following

```
   opt.add_option('--lv2', action='store_true', default=True, dest='lv2core',

```

replase dest=lv2 with dest=lv2core
