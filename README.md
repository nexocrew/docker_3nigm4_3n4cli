# Supported tags and respective `Dockerfile` links

-	[`0.1.0_beta`, `latest` (*0.1/Dockerfile*)](https://github.com/nexocrew/docker_3nigm4_3n4cli/0.1/Dockerfile)

# What is 3n4 cli client?
Official 3nigm4 command line application to access all 3nigm4 services. Now implements authentication and secure storage.

# How to use this image

## start a authserver instance

The following example require to mount as volume every directory contained files that should be manipulated and the keys directory (or the .3nigm4 dir under user's home directory).

```console
$ docker run -it --rm -v /home/user/.3nigm4:/root/.3nigm4:rw -v /filesdir/myfile.ext:/tmp/myfile.ext:ro nexo/3n4cli store upload -i /tmp/myfile.ext -O /root/.3nigm4/references/myfile.3n4 -M -v
```
