# What is a tar file?
Tar files are compressed files
just as zip files

# Why tar files?

Tar compression is very efficient compared to zip files.

file type 		.jpg 	.mp3 	.mp4 	.odt 	.png 	.txt

number of files 	2163 	45 	279 	2990 	2072 	4397
space on disk 		98M 	99M 	99M 	98M 	98M 	98M
tar 			94M 	99M 	98M 	93M 	92M 	89M
zip (no compression) 	92M 	99M 	98M 	91M 	91M 	86M
zip (deflate) 		87M 	98M 	93M 	85M 	77M 	28M
tar + gzip 		86M 	98M 	93M 	82M 	77M 	27M
tar + bz2 		87M 	98M 	93M 	42M 	71M 	22M
tar + xz 		70M 	98M 	22M 	348K 	51M 	19M

# Working wit tar files

Tar files come with tree diffirent types:

1.uncompressed .tar

2.compressed with gzip .tar.gz

3.compressed with bzip2 .tar.bz2

# Unpacking
```bash
tar -xvf file.tar

tar -xzvf file.tar.gz

tar -xjvf file.tar.bz2
```
more info working with tar files:

https://www.cyberciti.biz/faq/tar-extract-linux/



