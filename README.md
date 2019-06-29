# Visa Transaction Controls Postman Collections

> Inspired by [@Jeremy Thake](https://github.com/jthake-msft)'s [Microsoft Graph Collection](https://github.com/microsoftgraph/microsoftgraph-postman-collections/blob/master/README.md)

The Visa Transaction Controls Postman Collections is a community contributed open source repo to provide both the collection and the environment variable files to import into Postman.

The collection allows you to test common Visa Transaction Controls APIs from within Postman. Examples include registering a card, setting alerts, and running transactions to trigger alerts.

![Image of Postman](https://github.com/jcrosswh/vtc-postman-collections/blob/master/images/postman.png?raw=true)

Remember the best place to understand the workings of these APIs is to read our [Visa Transaction Controls API documentation](https://developer.visa.com/capabilities/vctc/docs).

## Setup

To setup the Postman collections follow these steps:

**1.** Download and register for [Postman](https://www.getpostman.com/).

**2.** Click **File | Import ...**.

**3.** Select **Import From Link**.

**4.** Paste the following two URLs and click Import after each.

`https://raw.githubusercontent.com/jcrosswh/vtc-postman-collections/master/Visa%20Developer%20VTC.postman_collection.json`

`https://raw.githubusercontent.com/jcrosswh/vtc-postman-collections/master/VTC%20Sandbox.postman_environment.json`

You should now see the **Visa Developer VTC** collection on the left had side Collections pane.

**5.** Click on the **No environment** drop down in top right hand corner.

**6.** Select **VTC Sandbox environment**.

**7.** Click the **eye** icon to the the right and then click **Edit**.

**8.** Enter in to the **current** (not **initial**) variables your VTC application: **PAN Prefix (Obtained from 'Test Data' on VDP)**, **UserId**, **FirstName**, **LastName**, and **Email**. Select **Update**. Close the **Manage Environments** dialog. 

**9.** Enter your credentials for each request. On the **VTC Sandbox environment** collection, click on the ellipsis to see more actions and select **Edit**. Select the **Authorization** tab. Under **Type** choose **Basic Auth**. Enter your **Username** and **Password** that is obtained from **'Credentials' on VDP**.

**10.** In the **VTC Sandbox environment** collection on left hand side, click on the **Register card** and click **Send** button on right hand side.  This call will give a document ID to associate to this card.  The document ID will be captured for you by the post call test.

**11.** Setup your email delivery by clicking on **Configuring alerts delivery** and clicking the **Send** button.  This will register your email address with the provided user ID.

**12.** Set rules on the card by sending either the **Turn off card by setting rules** call or the **Set alert conditions on card** call.  These rules will either always cause the card to be declined or set different alert conditions.

**13.** Run transactions on the card by sending in **Perform a cross border transaction** or **Perform a brick and mortar transaction** calls.

**14.** You can view alerts that may have been sent by using the **Get alerts by account number** call.

You are now up and running with VTC Postman collections.

## Contribute

You can contribute to this project by forking the repo and following the setup steps to import those files. When you've made your contributions in Postman editor, use the *File | Export* to overwrite the file in your forked branch. Then simply submit the forked branch as a PR back to this repo.