
----------

## _rootfs.ubifs_ >> file system directories

* ### _binwalk_ (Recommended)

```
sudo apt install binwalk
```

```
binwalk -e rootfs.ubifs
```
```
```





* _ubi_reader_

```
sudo pip install ubi_reader
```


* ubireader_extract_files <file_path>
```
ubireader_extract_files /home/gt/rootfs.ubifs
```

**Error**:<br><br>
<img src="https://github.com/Godson-Thomas/Root-File-System-261/blob/master/e_lzo.png" width="700">  <br><br>


**Solution**

* Download the lzo module. [_click here_](https://github.com/Godson-Thomas/Root-File-System-261/raw/master/lzo-2.10.tar.gz)
* Extract the file and enter into _lzo-2.10_ directory using the terminal
* Issue the following commands.

```
./configure
```
 Use _sudo_ for providing necessary permission
```
sudo make install
```
```
pip install python-lzo
```

* Use the _ubi_reader_ command

```
ubireader_extract_files /home/gt/rootfs.ubifs
```

------

## file system directories >> _rootfs.ubifs_

```
mkfs.ubifs -m 2048 -e 124KiB -c 2047 -r /media/GT/DIsk-3/RootFS/ubifs-root rootfs.ubifs
```

* - -m : min io size
* - -e : LEB size (Logical Erase Blocks)
* - -c : LEB count
* - -r : </path/to/your/rootfs/tree>

-------------