---
layout: post
title: docker registry v2 unique id
excerpt: The docker registry v2 does not support the query of the unique image id
tag:
 - docker
---
Consider the following use case: A docker deployment environment reads the registry to come up with inventory.
A "version object" in the inventory system is created for each tag and it is made unique with the digest.
The user persists a collection of version objects that make up their application as a snapshot (think: ui:03, database:latest, ...)
The snapshot is tested, staged, moved to production.

v1 allowed the creation of the version objects but no way to pull by digest

v2 won't support the creation of the version objects, but would allow them to be pulled.

The inventory system is IBM Urban Code Deploy, UCD.
The version objects are the UCD version objects.
Check out this [issue](https://github.com/docker/distribution/issues/46#issuecomment-77276022)

I personally don't think this is much of an issue.
Product teams should come up with unique tags for their docker images if they require snapshots to be dependable.
Making multiple UCD component version objects with identical tags will result in confusion.
