# spconv

This is a fork version of spconv original written by traverller52. I frozen those codes to here and add some of myself modifications. those codes released under Apache License.

Compare to origin implementation, I did those enhancement:

- remove all those unnessary codes exception the core algorithm;
- make it easy to built.



## Install

**note**: this lib does not support *gcc6+* built since there is a bug of nvcc, it will drop all `.cc` file which contains cuda to gcc to built, but gcc can not recognize those cuda codes. We have no good solution to make it work with gcc6+ but simply using gcc5 to compile it.

As far as I know, all torch extension written in cuda has this issue, include maskrcnn_benchmark repo (one of facebook official ).

to built **spconv**, simply:

```
# make sure your gcc version if 5
python3 setup.py bdist_wheel
cd dist
sudo pip3 install spconv-1.1-cp36-cp36m-linux_x86_64.whl
```

then everything is done.



## Copyright

the original copyright belongs to traveller52. I just did some tiny modifications and frozen most of it fuctionalities.

