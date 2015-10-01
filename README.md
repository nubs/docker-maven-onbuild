# docker-maven-onbuild
This is a base image for [java][java] [maven][maven] projects that can execute
simple applications [ONBUILD][ONBUILD].

## Purpose
This docker image builds on top of the [maven-build][maven-build] image, but
adds `ONBUILD` instructions to install the project code into the container and
execute `mvn`.

## Usage
This library is useful with a simple `Dockerfile`.  For example, using the
`Dockerfile`:

```dockerfile
FROM nubs/maven-onbuild:latest
```

you can build an image like so:

```bash
docker build --tag my-image .
```

To execute a command, you can simply:

```bash
docker run -it --rm my-image ./run
```

## License
docker-maven-onbuild is licensed under the MIT license.  See [LICENSE] for the
full license text.

[java]: http://java.com/
[maven]: https://maven.apache.org/
[ONBUILD]: https://docs.docker.com/reference/builder/#onbuild
[maven-build]: https://github.com/nubs/docker-maven-build
[LICENSE]: https://github.com/nubs/docker-maven-onbuild/blob/master/LICENSE
