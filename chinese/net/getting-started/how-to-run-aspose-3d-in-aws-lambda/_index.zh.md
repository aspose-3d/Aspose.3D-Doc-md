---
title: 如何在AWS Lambda中运行 Aspose.3D
type: docs
description: 使用Docker将 Aspose.3D 功能集成到您的应用程序中，无论您的开发堆栈采用何种技术。了解如何在Docker容器中使用 Aspose.3D
weight: 141
url: /zh/net/how-to-run-aspose-3d-in-aws-lambda/
---
## 准备AWS环境

1. 注册AWS账户:
[注册AWS账户](https://aws.amazon.com/)
1. 登录您的AWS账户，在您的账户下添加IAM用户。您可以参考AWS官方文档:
[添加IAM用户](https://docs.aws.amazon.com/IAM/latest/UserGuide/getting-started_create-admin-group.html)
1. 添加权限 “AmazonS3FullAccess”，请使用相同的方式，为每个添加EC2和Elastic Beanstalk，完全访问权限。
1. 在最后一步，确保您获得IAM用户名、密钥ID和 “credentials.csv” 文件，您需要很好地保存它们。
现在，请确保您的IAM用户具有S3，EC2，Elastic Beanstalk，完全访问权限。请参阅:
   
**![AWS Access](AwsAccess.png)**

## 安装AWS Toolkit for Visual Studio

1. 安装Visual Studio 2019或更高版本。
1. 下载并安装AWS Toolkit for Visual Studio:
[AWS工具包](https://aws.amazon.com/visualstudio/)

## 创建在AWS Lambda中运行的项目

1. 在Visual Studio中创建一个ASP .NET 核心Web应用程序，编写测试代码，从 nuget 获取 Aspose.3D。

1. 确保测试项目在本地计算机上运行良好，然后将其部署到AWS Elastic Beanstalk:
右键单击项目名称，选择 “发布到AWS Elastic Beanstalk”。(此选项仅在您安装AWS Toolkit for Visual Studio后存在)。
1. 您需要使用您的AWS账户和IAM用户添加新用户，您可以导入在上一步中获得的 “credentials.csv” 文件。
1. 发布成功，您将获得一个链接地址，如: `http://testprojectaspose-test.us-west-2.elasticbeanstalk.com/`
等10分钟链接生效，就可以访问了!
