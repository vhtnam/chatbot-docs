Stripe
==============


==============
Create Stripe Account
==============
- Open this url https://dashboard.stripe.com/register.
- Fill all require field in the Sign Up form then click on Create your Stripe account button.



==============
Getting API Keys
==============

- Open this url https://dashboard.stripe.com/account/apikeys.
- Click Reveal Secret key to get the Secret Key

.. image:: ../assets/images/get_stripe_api.jpg

==============
Configuration Stripe App
==============

- Login to Admin->Settings->Email, fill this form with your email credentials.
- Fill the Stripe Public Key and Secret and click Save.
.. image:: ../assets/images/admin_stripe.gif


==============
Configuration Stripe Webhook
==============

- After setting Client Id and Secret, Click Manage Webhook.

- Click Create Webhook.

- The Webhook List dialog will close, in the Stripe settings form, Click Save

.. image:: ../assets/images/admin_stripe_webhook.gif

==============
Troubeshotting
==============

1. Check if Stripe Plan creating.

- Go to Stripe Setting, scroll to bottom of the Page, click Manage.

.. image:: ../assets/images/admin_stripe1.gif

- Check if the Stripe Id Column of all Plan (exept Free plan) is not empty.

.. image:: ../assets/images/admin_stripe2.gif

- If there, click Sync for this Plan.

2. Check if Webhook is running.

- Try in the Test mode, upgrade a Bot to any Pro plan.

- If the Payment success, go to  https://stripe.com/  and login with your Stripe Account.
 
- On the left sidebar, click Developers->Webhook. If your app is in test mode, swith to Test Data.

.. image:: ../assets/images/admin_stripe3.gif

- Click to the webhook of your site.

.. image:: ../assets/images/admin_stripe4.gif


- Scroll down to the Webhook Events section.

- Check if there is a success webhook event with name invoice.payment_succeeded in the event list at the time you upgrade your Bot.

.. image:: ../assets/images/admin_stripe5.gif

- If not, recheck your Paypal Webhook Setting.