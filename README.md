## _rootfs.ubifs_ >> file system directories

* _ubi_reader_

```
sudo pip install ubi_reader
```


* ubireader_extract_files <file_path>
```
ubireader_extract_files /home/gt/rootfs.ubifs
```

**Error**:<br><br>
<img src="https://github.com/Godson-Thomas/dccp/blob/master/e_lzo.png" width="700">  <br><br>


**Solution**

* Download the lzo module. [_click here_]()
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
