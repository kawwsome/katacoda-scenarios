Before we get into package installation and the different managers, we need to discuss archiving and compressing files, because you will most likely encounter these when you hunt for software on the internet.

You probably already know what a file archive is, you've most likely encountered file types such as .rar and .zip. These are an archive of files, they contain many files inside of them, but they come in this very neat single file known as an archive.

**Compressing files with gzip**

gzip is program used to compress files in Linux, they end in a .gz extension.

To compress a file down:
```
$ gzip mycoolfile
```

To decompress the file:
```
$ gunzip mycoolfile.gz
```

**Creating archives with tar**
Unfortunately, gzip can't add multiple files into one archive for us. Luckily we have the tar program which does. When you create an archive using tar, it will have a .tar extension.

```
$ tar cvf mytarfile.tar mycoolfile1 mycoolfile 2
```

* c - create
* v - tell the program to be verbose and let us see what it's doing
* f - the filename of the tar file has to come after this option, if you are creating a tar file you'll have to come up with a name

**Unpacking archives with tar**

To extract the contents of a tar file, use:

```
$ tar xvf mytarfile.tar
```

* x - extract
* v - tell the program to be verbose and let us see what it's doing
* f - the file you want to extract

**Compressing/uncompressing archives with tar and gzip**

Many times you'll see a tar file that has been compressed such as: mycompressedarchive.tar.gz, all you need to do is work outside in, so first remove the compression with gunzip and then you can unpack the tar file. Or you can alternatively use the **z** option with tar, which just tells it to use the gzip or gunzip utility.

Create a compressed tar file:
```
$ tar czf myfile.tar.gz
```

Uncompress and unpack:
```
$ tar xzf file.tar
```

If you need help remember this: e**X**tract all **Z**ee **F**iles!

tar is one of those commands that is so important and yet you never really remember it, relevant xkcd: <a href="https://xkcd.com/1168/">https://xkcd.com/1168/</a>

**Other Utilities**

Throughout your journey of Linux, you'll encounter other archive and compression types such as: bzip2, compress, zip, unzip, etc. They are a little less common, but just keep in mind that different utilities will call for different commands.

## Exercise

Familiarize yourself with the tar documentation and look at the other options available in the manpage.

>>Q1: What tar flag is used to create archives?<<
=== c
