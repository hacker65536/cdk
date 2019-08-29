

ref
--
https://github.com/aws/aws-cdk/issues/1305


solution
--

```typescript
import cdk = require("@aws-cdk/core");
import ec2 = require("@aws-cdk/aws-ec2");
import { Vpc, SubnetType } from "@aws-cdk/aws-ec2";

export class LambdabackedcustomresourcesStack extends cdk.Stack {
  constructor(scope: cdk.Construct, id: string, props?: cdk.StackProps) {
    super(scope, id, props);

    // The code that defines your stack goes here

    const vcp = new Vpc(this, "vpc", {
      maxAzs: 2,
      //natGateways: 0,
      subnetConfiguration: [{ name: "pub", subnetType: ec2.SubnetType.PUBLIC }]
    });
  }
}
```
