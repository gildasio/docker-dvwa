# DVWA Docker

A minimal [Docker] image with [Damn Vulnerable Web Application (DVWA)][dvwa] to you enjoy.

## Use

To use you need docker:

~~~
$ docker pull gjuniioor/dvwa:latest
$ docker run -d -p 80:80 gjuniioor/dvwa
~~~

And go to [localhost:80][local]

## Tags

* **latest**: development source
* **1.9**: with the 1.9 version of DVWA
* **1.0.8**: with the 1.0.8 version of DVWA

## Bugs

Has a bug found? Please, open a [Issue], a [Pull Request][pr] or contact me: [@gjuniioor]. 

[docker]: https://www.docker.com/
[dvwa]: http://dvwa.co.uk/
[local]: http://localhost:80
[issue]: https://github.com/gjuniioor/docker-dvwa/issues
[pr]: https://github.com/gjuniioor/docker-dvwa/pulls
[@gjuniioor]: https://github.com/gjuniioor
