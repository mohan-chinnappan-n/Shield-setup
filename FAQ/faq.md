# FAQ - Shield


 1.How do I know a Field in an Object is encrypted at rest?
 --------------------------------------------------------

Metadata API - ***describe*** - provides **encrypted** flag for this encrypted field as **true** as shown below:

#### Account object encrypted fields:

![Account object encrypted fields:](img/account-encrypted-fields.png)

#### Describe on Account Object showing encrypted fields:

![describe showing the encrypted flag](img/describe-showing-encrypted-flag.png)


#### Describe on Account Object:

![describe showing the Account Object](img/account-describe-metadata.png)



2.Knowledge Article: 000247422 says: View Encrypted Data Permission Not Needed with Shield Platform Encryption Beginning Spring ‘17
---------------------------------------------------------------------------------------------------------------------------------
Can you explain this with an example?
-------------------------------------

![KB-FLS](img/KB-FLS.png)
[Reference to this Knowledge Article](https://help.salesforce.com/articleView?id=000247422&type=1)


![Winter17 release-notes](img/win17-rel-notes-viewEncryptedData-perm-NN.png)


[Reference: View Encrypted Data” Permission Not Needed with Shield Platform Encryption Beginning Spring ‘17](https://releasenotes.docs.salesforce.com/en-us/winter17/release-notes/rn_security_pe_ved_decouple_announcement.htm)



Let us take an example: In our org, we have an user: **joe simple**

![user joe simple](img/user-joe-simple.png)


Joe can see the **encrypted** field: **Account.Fax** but Joe **can't** see the **encrypted** field **Account.Phone** as per FLS for his profile:

#### Account.Fax:
![joe account.fax](img/user-joesimple-can-seee-account_fax.png)


#### Account.Phone:
![joe account.phone](img/user-joesimple-cannot-see-account_phone.png)



If Joe uses REST API for example, to access Joe will be denied access to this field **Account.Fax** as shown below:

![joe cannot access account.phone](img/rest-api-user-cannot-access_account_phone.png)

But other user, whose FLS allows **read** on these fields: **Account.Fax** and **Account.Phone** can access these two fields:


![describe showing the encrypted flag](img/describe-showing-encrypted-flag.png)



3. Can you provide technical details about Platform Encryption?
----------------------------------------------------------------

[![Everything Is AWESOME](//img.youtube.com/vi/RMUl0fF7x1E/0.jpg)](//www.yout‌​ube.com/watch?v=RMUl0fF7x1E "Salesforce Shield Platform Encryption Whiteboard")
