# CDK_Ziua3
oridnea comenzilor de pe -> https://docs.aws.amazon.com/cdk/latest/guide/hello_world.html.

Am rulat:
- cdk init --language python.
- source pt environment.
- pip install requirements.txt.
- pip install aws-cdk.aws-s3.

Adaugat in ziua3/ziua3_stack.py:
- from aws_cdk import aws_s3 as s3
- "bucket = s3.Bucket(self, 
    "MyFirstBucket", 
    versioned=True,)";

Syntetizat codul pt stack: cdk synth; verificat in /cdk.out/Ziua3Stack.template.json stack-ul.

Deploy: cdk deploy

Modificari facute in ziua3/ziua3_stack.py pentru deletion policy, cdk diff pentru a vedea modificarile, cdk deploy pt alt deploy si verificat in .json modoficarea facuta pe stack. 
cdk bootstrap aws://unknown-account/unknown-region (cerut pt credentiale)