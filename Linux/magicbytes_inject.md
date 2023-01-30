# Magicbytes

[File signatures](https://en.wikipedia.org/wiki/List_of_file_signatures) are also known as magic numbers or Magic Bytes.

## Inject

On Linux operating systems you can inject the file signature of one file to another file. Note, that example.jpg has to be a legit .jpg file.
<br></br>
```bash

head -c example.jpg > example.txt
```

Now example.txt is recognized as a .jpg file on a linux environment. This can be used to bypass file upload filters on webapps.