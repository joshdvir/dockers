## SAWS

Dockerized SAWS

[https://github.com/donnemartin/saws](https://github.com/donnemartin/saws)


## Add an alias to your .bashrc / .zshrc

```
alias cfn-flip='docker run -it --rm -v `pwd`:/workdir joshdvir/saws'
```

## Docker image

[https://hub.docker.com/r/joshdvir/saws](https://github.com/awslabs/saws)

The Docker images is [Whalebrew](https://github.com/bfirsh/whalebrew) ready so if you are using Whalebrew run

`
whalebrew install joshdvir/saws
`