Saleforces
==============
.. Note:: Your site must run under https to allow salesforce integration.

.. Note:: You will need one of those Salesforce account: : Group, Professional, Enterprise, Performance, Unlimited, and Developer Editions.

==============
Create a Connected Salesforce App
==============

- Sign in to your Salesforce.com developer account. If you were in Salesforce Classic, switch to Lightning Experience
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce-1.jpg
- Click Setup button located on top right of the header.
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce-1.jpg
- In the left navigation column, under App Setup, select App Manager
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce2-1.jpg
- In the Connected Apps section, click New.
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce3.jpg

- Complete the Basic Information, and in the API section, select Enable OAuth Settings.
- In the new OAuth settings that appear, for Callback URL, type the fully qualified domain name of your server, using the https protocol, and append the following text to the URL:  https://your_site_domain/auth/integration/salesforce/callback

For example:
Move the following items from Available OAuth Scopes to Selected OAuth Scopes:
- Access and manage your data (api)
- Access your basic information (id)
- Perform requests on your behalf at any time (refresh_token)

.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce4-2.jpg

- Click Save



==============
Get API Credentials
==============

- Back to App Manager, scroll to your new app, click More Button, select View.
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce5.jpg

- In next screen, you will get your App credentials
.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce6.jpg
- After you save the app, Salesforce populates the API section with the following IDs that you will use to configure: Consumer Key, Consumer Secret, Callback URL.

==============
Integrate with your site
==============

Open Administration page, navigate to Settings->Integrations. Fill the Salesforce form with following value:

   - Consumer Key
   - Consumer Secret
   - Callback URL: https://your_site_domain/auth/integration/salesforce/callback
   - Login URL: https://login.salesforce.com

.. image:: https://landingmall.stsengine.com/wp-content/uploads/sites/5/2018/08/salesforce.jpg

