# vaccineavailability

VaccineNotifier checks the cowin portal periodically to find vaccination slots available in your pin code and for your age. If found, it will send you emails every minute until the slots are available.

Steps to run the script:

Step 1) Enable application access on your gmail with steps given here: https://support.google.com/accounts/answer/185833?p=InvalidSecondFactor&visit_id=637554658548216477-2576856839&rd=1

Step 2) Enter the details in the file .env, present in the same folder

Ex :- 
PINCODE=560066
EMAIL=pragtyag@gmail.com
APPLICATION_PASSWORD=<The 16 digit code you will get after giving application access to your gmail >     (for ex :- fnuzrlpkzuklm***)
AGE=65

Step 3) On your terminal run: npm i && pm2 start vaccineNotifier.js

To close the app run: pm2 stop vaccineNotifier.js && pm2 delete vaccineNotifier.js

Now npm is a node.js application and pm is a application manager . Steps to install these are as follows :- 
https://phoenixnap.com/kb/install-node-js-npm-on-windows

Installing pm2 on windows 
if npm is installed then you need to run following command on command prompt:- npm install pm2 -g 

Here's a sample of the resultant emails: 

![image](https://user-images.githubusercontent.com/83806389/117409063-60a95a80-af2e-11eb-818c-658191a55163.png)

After starting application you will get following on the command prompt 

![image](https://user-images.githubusercontent.com/83806389/117410213-c21df900-af2f-11eb-8ebf-ea2cacfccecf.png)

Now if you make any changes in the env file for ex like age group filter or pin code filter then you need to stop the application and then change env file save it and then restart the application . After stopping the application you will find screenshot like this . 

![image](https://user-images.githubusercontent.com/83806389/117410663-5c7e3c80-af30-11eb-874d-ed5bf0a0e5e9.png)

Also you need to ensure you add all the application files like env, notififer and vaccinenotifer in your laptop root directory . Usually in C:/user/<admin user> directory


