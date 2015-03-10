---
layout: post
title: fetch image tags and hashes
excerpt: The latest docker registry api spec supports the retrieval of image tags and image hashes.
---
{{ page.excerpt }}

See [tarsum spec](https://github.com/openshift/origin/blob/master/Godeps/_workspace/src/github.com/docker/docker/pkg/tarsum/tarsum_spec.md)
See [Docker Registry HTTP API V2](https://github.com/docker/distribution/blob/master/doc/spec/api.md)

# tarsum
The tarsum normalizes a tar (sorting by file name, sorting extending attribute headers) and removes some information (timestamps) before calculating a hash.
Specifically the hash includes the file contents and the following file attributes:

- name - file name
- mode - read, write, execute, ...
- uid - user id
- gid - group id
- size - size of file
- typeflag - file, directory, symlink, hardlink
- linkname - if link
- uname - user name
- gname - group name
- devmajor - for device
- devminor - for device
- extented attribute headers ("SCHILY.xattr." prefixed pax headers)

