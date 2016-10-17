docker-openrefine
=================

A Dockerfile setting up OpenRefine with rdf extension:

- [RDF extension][1] to bring Linked Data capabilities to OpenRefine

Run the docker
--------------

This docker is hosted on the [official docker.io hub][2]. Running it is as simple as:

    docker run -p 80:3333 armandobs/docker_openrefine

If you want refine projects to be persistent, you must mount `/mnt/refine` as follows:

    docker run -p 80:3333 -v /path-to-host:/mnt/refine armandobs/docker_openrefine

You can also increase the max size of the heap, by specifying the REFINE_MEMORY environment variable:

    docker run -p 80:3333 -e REFINE_MEMORY=24G armandobs/docker_openrefine

Observations
------------
This project is based on [3].

References
----------
[1]: https://github.com/fadmaa/grefine-rdf-extension
[2]: https://registry.hub.docker.com/u/armandobs/docker_openrefine/
[3]: https://github.com/SpazioDati/docker-openrefine
