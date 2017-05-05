# JarCleaner
Simple tool for cleaning jar files

## Description
Application will be used to clean directory from library duplicates. Application should pick the most recent version of the library and remove the rest of its instances.

## Used technologies
- Application is written in C++.
- Application can be built under Windows or Linux.
- Uses Qt libraries.
- Uses boost headers.
- Windows: Project can be built with Visual Studio Community.
- Linux: Project can be build with gcc.

### Usage
_JarCleaner_ DIRECTORY_TO_CLEAN [--dry-run]

DIRECTORY_TO_CLEAN - path to the directory containing jar files.
--dry-run - Application will just print the list of files to delete.

### Supported version formats
```
NAME-VERSION[-RELEASE][-SNAPSHOT]
```

#### VERSION
Chain of numbers separated by ".". e.g. 1.2.3, 1 or 1.2.3.4.5.6

#### RELEASE
Special tag with release name. Tags must be comparable.
General rule:
snapshot < rc < ga < release = final

#### SNAPSHOT
Sometime there could be third version chunk "-SNAPSHOT". It could be ignored except situation where it is the only diffrence in the version. Then file with an extra -SNAPSHOT should be deleted.

### Rules file
TODO

### Unit tests
TODO
