# aws-cfn-template-flip

Dockerized aws-cfn-template-flip so we can convert all our JSON CF template to YAML.

[https://github.com/awslabs/aws-cfn-template-flip](https://github.com/awslabs/aws-cfn-template-flip)

## Add an alias to your .bashrc / .zshrc

```
alias cfn-flip='docker run -it --rm -v `pwd`:/root joshdvir/aws-cfn-template-flip'
```

## Docker image

[https://hub.docker.com/r/joshdvir/aws-cfn-template-flip](https://github.com/awslabs/aws-cfn-template-flip)
