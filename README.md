### Cloudormation template toolbox

Currently two tools are installed

* cfn-lint - [lint your cloudformation templates](https://github.com/aws-cloudformation/cfn-python-lint)
* cfn-flip - [converts AWS CloudFormation templates between JSON and YAML formats](https://github.com/awslabs/aws-cfn-template-flip)

If you need add new tools, raise ticket in https://github.com/alpine-docker/cfn/issues

### Usage

```
# cd to the folder where you put the cloudformation templates
# for example, the template file name is `template.yaml`


# lint check cloudformation template file
$ docker run -ti --rm -v $(pwd):/data -w /data alpine/cfn cfn-lint template.yaml

# converts AWS CloudFormation templates between JSON and YAML formats
$ docker run -ti --rm -v $(pwd):/data -w /data alpine/cfn cfn-flip template.yaml
```
