# API Reference

**Classes**

Name|Description
----|-----------
[BashExecFunction](#cdk-lambda-bash-bashexecfunction)|*No description*


**Structs**

Name|Description
----|-----------
[BashExecFunctionProps](#cdk-lambda-bash-bashexecfunctionprops)|*No description*
[RunOps](#cdk-lambda-bash-runops)|*No description*



## class BashExecFunction  <a id="cdk-lambda-bash-bashexecfunction"></a>



__Implements__: [IConstruct](#constructs-iconstruct), [IDependable](#constructs-idependable)
__Extends__: [Construct](#constructs-construct)

### Initializer




```ts
new BashExecFunction(scope: Construct, id: string, props: BashExecFunctionProps)
```

* **scope** (<code>[Construct](#constructs-construct)</code>)  *No description*
* **id** (<code>string</code>)  *No description*
* **props** (<code>[BashExecFunctionProps](#cdk-lambda-bash-bashexecfunctionprops)</code>)  *No description*
  * **script** (<code>string</code>)  The path of the shell script to be executed. 
  * **dockerfile** (<code>string</code>)  The path of your custom dockerfile. __*Optional*__
  * **environment** (<code>Map<string, string></code>)  Lambda environment variables. __*Optional*__
  * **role** (<code>[aws_iam.IRole](#aws-cdk-lib-aws-iam-irole)</code>)  Custom lambda execution role. __*Default*__: auto generated role.
  * **securityGroups** (<code>Array<[aws_ec2.ISecurityGroup](#aws-cdk-lib-aws-ec2-isecuritygroup)></code>)  Custom lambda execution securityGroups. __*Default*__: auto generated securityGroups.
  * **timeout** (<code>[Duration](#aws-cdk-lib-duration)</code>)  The function execution time (in seconds) after which Lambda terminates the function. __*Default*__: Duration.seconds(60)
  * **vpc** (<code>[aws_ec2.IVpc](#aws-cdk-lib-aws-ec2-ivpc)</code>)  Custom lambda execution vpc. __*Default*__: auto generated vpc.
  * **vpcSubnets** (<code>[aws_ec2.SubnetSelection](#aws-cdk-lib-aws-ec2-subnetselection)</code>)  Custom lambda execution vpcSubnets. __*Default*__: auto generated vpcSubnets.



### Properties


Name | Type | Description 
-----|------|-------------
**handler** | <code>[aws_lambda.DockerImageFunction](#aws-cdk-lib-aws-lambda-dockerimagefunction)</code> | <span></span>

### Methods


#### run(ops?) <a id="cdk-lambda-bash-bashexecfunction-run"></a>



```ts
run(ops?: RunOps): CustomResource
```

* **ops** (<code>[RunOps](#cdk-lambda-bash-runops)</code>)  *No description*
  * **runOnUpdate** (<code>boolean</code>)  whether to run the lambda function again on the provider update. __*Default*__: false;

__Returns__:
* <code>[CustomResource](#aws-cdk-lib-customresource)</code>



## struct BashExecFunctionProps  <a id="cdk-lambda-bash-bashexecfunctionprops"></a>






Name | Type | Description 
-----|------|-------------
**script** | <code>string</code> | The path of the shell script to be executed.
**dockerfile**? | <code>string</code> | The path of your custom dockerfile.<br/>__*Optional*__
**environment**? | <code>Map<string, string></code> | Lambda environment variables.<br/>__*Optional*__
**role**? | <code>[aws_iam.IRole](#aws-cdk-lib-aws-iam-irole)</code> | Custom lambda execution role.<br/>__*Default*__: auto generated role.
**securityGroups**? | <code>Array<[aws_ec2.ISecurityGroup](#aws-cdk-lib-aws-ec2-isecuritygroup)></code> | Custom lambda execution securityGroups.<br/>__*Default*__: auto generated securityGroups.
**timeout**? | <code>[Duration](#aws-cdk-lib-duration)</code> | The function execution time (in seconds) after which Lambda terminates the function.<br/>__*Default*__: Duration.seconds(60)
**vpc**? | <code>[aws_ec2.IVpc](#aws-cdk-lib-aws-ec2-ivpc)</code> | Custom lambda execution vpc.<br/>__*Default*__: auto generated vpc.
**vpcSubnets**? | <code>[aws_ec2.SubnetSelection](#aws-cdk-lib-aws-ec2-subnetselection)</code> | Custom lambda execution vpcSubnets.<br/>__*Default*__: auto generated vpcSubnets.



## struct RunOps  <a id="cdk-lambda-bash-runops"></a>






Name | Type | Description 
-----|------|-------------
**runOnUpdate**? | <code>boolean</code> | whether to run the lambda function again on the provider update.<br/>__*Default*__: false;



