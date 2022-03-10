+++
title = "Backend"
weight = 12
+++

## How it works

* The front-end application uses a local languages resource file to substitute language strings when the locale is changed. 
* You will download this file and use a Node function that uses Amazon Translate to create a new file with a range of translations.
* After the new language file is created, you will copy it into the frontend code and republish through Amplify Console.
* Finally you will reload the front-end and test the new language functionality.

### Step-by-step instructions ###

1. Go to the AWS Management Console, click **Services** then select [**Cloud9**](https://console.aws.amazon.com/cloud9) under Developer Tools. **Make sure your region is correct.**
2. In the left panel of the IDE, open the ```codes/4-translate/local-app``` folder in the aws-serverless-workshop-innovator-island directory. Click on ```translations-input.json``` to see the English input language file.
3. **Please Write a ```translate.js``` file to locally to translate the input file.** 
4. Please choose your target languages as Chinese.

 
### Starting the translation process

1. Run the local  application to use Amazon Translate to create the translation file.  Example command:

```
node ./translate.js $AWS_REGION
```

5. After a few seconds, the function completes and has created a new file in the same directory called ```translations.json```. Click on the file in the left panel of the IDE to inspect the contents. You will see it contains translations of the string resources in the target languages.
