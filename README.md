# Docker Image Converter

## Usage

```
Usage: ./convert.py tarball lazifier

  tarball
       The image.tar created by docker save.

  lazifier
       A command which takes 3 arguments: <root>, <meta>, and <pool>.
       It will traverse the <root> directory tree, save the tree structure in <meta>,
       and stash the content of regular files into the <pool> based on its sha256sum.
```

## Example

```bash
# the tarball to convert
docker save -o hello.tar hello:latest

# use cafs/convert as the external lazifier
./convert hello.tar ~/cafs/tools/convert
```
