### Procedure to Setup WAF:

## Step 1: Verify IAM user has the proper access to AWS managed WAF policies:
1. Take necessary permissions from the administrator for AWS managed WAF policies

## Step 2: Search WAF & Shield service in the search bar:
1. Click on WAF & Shield to open the service.

## Step 3: Create a Web ACL:
1. To create a web ACL
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF3.png)
2. Choose to Create web ACL
3. On Name Block, enter the name you want to use to identify this web ACL
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF4.png)
4. On Description block – type a description for the web ACL.
5. On CloudWatch metric name block, type the name you want. Then, check the guidance on the console for valid characters.
6. On the resources type block, select CloudFront distributions or regional resources based on your requirement from the below options.
7. For Associated AWS resources – choose Add AWS resources if you select regional resources. In the dialog box, select the resources that you want to use, and then select Add.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF5.png)
8. Choose Next.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF6.png)

## Step 4: Add an AWS Managed Rules rule group
1. To add an AWS Managed Rules rule group.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF7.png)

2. On the Add rules and rule groups page, choose Add rules and add managed rule groups.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF8.png)

3. On the Add managed rule groups page, view the AWS managed rule groups listing. (You can also choose listings offered for AWS Marketplace sellers. You can subscribe and use them in the same way as for AWS Managed Rules rule groups.)
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF10.png)

4. For the rule group that you want to add. In the Action column, turn on the Add to web ACL toggle.

![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF11.png)

5. Select Edit and, in the rule group’s Rules listing, turn on the set all rule actions to count toggle. It sets the action for all rules in the rule group to count only. It lets you see how all the rules in the rule group behave with your web requests before you put any of them to use.

6. Choose Save rule. In the Add managed rule groups page, choose Add rules. It returns you to the Add rules and rule groups page.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF13.png)

## Step 5: Finish your Web ACL configuration:
1. To finish your web ACL configuration
2. On the Add rules and rule groups page, choose Next.
3. You can see the processing order for the rules and rule groups in the web ACL on the Set rule priority page. AWS WAF processes them starting from the top.

![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF12.png)
4. Choose Next.
5. On the Configure metrics page, you can see the planned metrics for your rules and rule groups and you can see the web request sampling options
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF132.png)
6. Choose Next.
7. On the Review and create web ACL page, click on Create web ACL.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF14.png)

8. The wizard returns you to the Web ACL page, where your new web ACL is listed.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF151.png)

![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF16.png)


## Step 6: Monitor WAF Metrics:
1. Open the CloudWatch page and click on Metrics from the left column.
![alt text](https://d5q4akjun1yjt.cloudfront.net/assets/WAF17.png)
2. Select the AWS WAF metrics and select the rules for the required graph


