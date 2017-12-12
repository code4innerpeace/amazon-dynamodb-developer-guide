# UntagResource<a name="API_UntagResource"></a>

Removes the association of tags from an Amazon DynamoDB resource\. You can call UntagResource up to 5 times per second, per account\. 

For an overview on tagging DynamoDB resources, see [Tagging for DynamoDB](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Tagging.html) in the *Amazon DynamoDB Developer Guide*\.

## Request Syntax<a name="API_UntagResource_RequestSyntax"></a>

```
{
   "ResourceArn": "string",
   "TagKeys": [ "string" ]
}
```

## Request Parameters<a name="API_UntagResource_RequestParameters"></a>

The request accepts the following data in JSON format\.

**Note**  
In the following list, the required parameters are described first\.

 ** ResourceArn **   
The Amazon DyanamoDB resource the tags will be removed from\. This value is an Amazon Resource Name \(ARN\)\.  
Type: String  
Length Constraints: Minimum length of 1\. Maximum length of 1283\.  
Required: Yes

 ** TagKeys **   
A list of tag keys\. Existing tags of the resource whose keys are members of this list will be removed from the Amazon DynamoDB resource\.  
Type: Array of strings  
Length Constraints: Minimum length of 1\. Maximum length of 128\.  
Required: Yes

## Response Elements<a name="API_UntagResource_ResponseElements"></a>

If the action is successful, the service sends back an HTTP 200 response with an empty HTTP body\.

## Errors<a name="API_UntagResource_Errors"></a>

For information about the errors that are common to all actions, see [Common Errors](CommonErrors.md)\.

 **InternalServerError**   
An error occurred on the server side\.  
HTTP Status Code: 500

 **LimitExceededException**   
Up to 50 `CreateBackup` operations are allowed per second, per account\. There is no limit to the number of daily on\-demand backups that can be taken\.   
Up to 10 simultaneous table operations are allowed per account\. These operations include `CreateTable`, `UpdateTable`, `DeleteTable`,`UpdateTimeToLive`, and `RestoreTableFromBackup`\.   
For tables with secondary indexes, only one of those tables can be in the `CREATING` state at any point in time\. Do not attempt to create more than one such table simultaneously\.  
The total limit of tables in the `ACTIVE` state is 250\.  
For tables with secondary indexes, only one of those tables can be in the `CREATING` state at any point in time\. Do not attempt to create more than one such table simultaneously\.  
The total limit of tables in the `ACTIVE` state is 250\.  
HTTP Status Code: 400

 **ResourceInUseException**   
The operation conflicts with the resource's availability\. For example, you attempted to recreate an existing table, or tried to delete a table currently in the `CREATING` state\.  
HTTP Status Code: 400

 **ResourceNotFoundException**   
The operation tried to access a nonexistent table or index\. The resource might not be specified correctly, or its status might not be `ACTIVE`\.  
HTTP Status Code: 400

## See Also<a name="API_UntagResource_SeeAlso"></a>

For more information about using this API in one of the language\-specific AWS SDKs, see the following:

+  [AWS Command Line Interface](http://docs.aws.amazon.com/goto/aws-cli/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for \.NET](http://docs.aws.amazon.com/goto/DotNetSDKV3/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for C\+\+](http://docs.aws.amazon.com/goto/SdkForCpp/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for Go](http://docs.aws.amazon.com/goto/SdkForGoV1/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for Java](http://docs.aws.amazon.com/goto/SdkForJava/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for JavaScript](http://docs.aws.amazon.com/goto/AWSJavaScriptSDK/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for PHP V3](http://docs.aws.amazon.com/goto/SdkForPHPV3/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for Python](http://docs.aws.amazon.com/goto/boto3/dynamodb-2012-08-10/UntagResource) 

+  [AWS SDK for Ruby V2](http://docs.aws.amazon.com/goto/SdkForRubyV2/dynamodb-2012-08-10/UntagResource) 