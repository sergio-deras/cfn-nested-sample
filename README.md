# cfn-nested-sample
Simple CloudFormation nested stack


## USING SAM
### PYTHON VENV
```bash
cd sam-express-sample
python3 -m venv venv
source venv/bin/activate
```

### SAM
Using sam-nw as stack name
```
pip install aws-sam-cli
sam build -t template-sam.yaml
sam deploy -g 
aws cloudformation delete-stack --stack-name sam-nw
```

## USING CFN
Using cfn-nw as stack name
```
aws cloudformation package --template-file template-cfn.yaml --output-template packaged.yaml --s3-bucket <your-bucket>
aws cloudformation deploy --template-file packaged.yaml --stack-name cfn-nw 
aws cloudformation delete-stack --stack-name cfn-nw
```

