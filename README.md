# awsbedrock-demo

The following files are added as part of this demo:

Business/BusinessFunction.py
This lambda function is configured in Action Group.

Business/BusinessSchema.json
This is the Open API Schema configured in Action Group.

Business/kb-data
Here you will find two (knowledge base) files used in the demo:
ProductCatalog.csv, ProductDescriptions.pdf

Businesse/InvokeAgentBusiness.py
This is a lambda function to invoke the Business Agent programmatically.
If you don't plan to invoke the Agent programmatically, you can ignore it.
You must use a version of boto3 that supports bedrock-agent-runtime (eg. version 1.34.49).

#Steps for setup:
1. Gain access to foundational model (In AWS Console > Bedrock > Foundation Models > Base Model > Model Access > Manage Model Access > Select the Models you need access to and hit Save)
2. Create agent (Clause 3.5 Sonnet was used for this demo)
3. Create knowledgebase by uploading the files to s3 bucket and pointing this as source. Use vector embeddings
4. For action group, use the lambda function code provided. Configure IAM roles accordingly. BusinessSchema.json - This is the Open API Schema configured in Action Group.
5. Create alias as required to capture model behaviour at different points
6. Prepare and test the agent through the chat interface
