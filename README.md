# Installation of netCDF libraries (Linux and Darwin)

`sudo apt install libnetcdf-dev libnetcdf-c++4-dev`


### How to compile and link (debian)
Need to find where those libraries are, specifically the libnetcdf_c++4:
`sudo find /usr -name libnetcdf*`

```
/usr/share/doc-base/libnetcdf-c++4-doc.netcdf-cxx
/usr/share/doc/libnetcdf-c++4-doc
/usr/share/doc/libnetcdf-c++4-1
/usr/share/doc/libnetcdf-dev
/usr/share/doc/libnetcdf19
/usr/share/doc/libnetcdf-c++4-dev
/usr/share/doc/libnetcdf-c++4
/usr/share/lintian/overrides/libnetcdf-dev
/usr/share/lintian/overrides/libnetcdf-c++4
/usr/lib/x86_64-linux-gnu/libnetcdf_c++4.so.1.1.0
/usr/lib/x86_64-linux-gnu/libnetcdf_c++.so.4
/usr/lib/x86_64-linux-gnu/libnetcdf.so.19
/usr/lib/x86_64-linux-gnu/libnetcdf_c++4.so
/usr/lib/x86_64-linux-gnu/libnetcdf_c++.so.4.2.0
/usr/lib/x86_64-linux-gnu/libnetcdf.settings
/usr/lib/x86_64-linux-gnu/libnetcdf_c++4.a
/usr/lib/x86_64-linux-gnu/libnetcdf.so
/usr/lib/x86_64-linux-gnu/libnetcdf_c++4.so.1
```

and now we  can specify absolute paths via -L option:

`g++ main.cpp -L /usr/lib/x86_64-linux-gnu/ -lnetcdf_c++4 -o test`