# Mailchimp Email Templates from OrderCloud.io

The [OrderCloud Platform](https://ordercloud.io/) is a great way to solve complex B2B eCommerce and order management challenges. But a key part of eCommerce is emails! Users expect emails when they place an order, get a shipment, etc. The OrderCloud platform provides a powerful tool to trigger emails based on OC Platform events: Message Senders. 

We provide a built-in Message Sender configuration to use with [MailChimp/Mandrill](https://mandrill.com/), but if you have a different preferred email sender, such as SendGrid or others, you can write your own custom Message Sender. See our documentation [here]().

If you'd like to proceed with the Mandrill Message Sender, you need the following:

1. A MailChimp account with [the Mandrill Transactional Email add-on](http://kb.mailchimp.com/mandrill/add-or-remove-mandrill)
2. Your Mandrill API Key (this can be found in your Mandrill Settings page)[1]

[1]: If you'd just like to try out the Mandrill Message Sender, no problem! You can set up a message sender without a Mandrill API Key. However, this API key allows only a limited number of sends, and more importantly, uses the default OrderCloud-branded email templates! Get your own paid Mandrill account to configure your own custom email templates. 

## Configure OC Platform Message Sender

### Create The Message Sender
1. Go to your [OrderCloud Dashboard](https://dashboard.ordercloud.io), and select the Organization that you'd like to configure a Message Sender for. Message Senders are configured at the organization level.
2. Select "Message Senders" from the left nav.
3. Hit "New"
4. Add a name to your message sender, so you can distinguish it at a glance.
5. If using the test API key, you're set. If using your own API key, check the box next to "Use My Mandrill Account", and enter in your own Mandrill API key.
6. Next, you'll see a list of the various emails the default Mandrill Message Sender allows you to send. Enable the emails you'd like to send.
7. Finally, hit "Create Message Sender"

You now have a message sender! However, you're not done just yet. :)

### Assign The Message Sender

1. In the [Console](https://console.ordercloud.io/), open the Seller Application that you'd like to set up emails for. 
2. Under "Seller", find "Message Senders" and select it.
3. List your message senders. You'll see the message sender you just created, along with the configured message types for that sender.
4. Assign that message sender to the buyer or user group that you want. This allows you to configure different emails for different buyers-- Buyer A wants a reply email that reflects their company name but Buyer B wants their own company name there? Buyer C uses Mandrill but Buyer D uses Sendgrid? You're set.

## Configure MailChimp/Mandril

So, OrderCloud is all set up, but if you tried to trigger an email right now, you wouldn't get one. This is because OrderCloud is sending Mandrill data, but Mandrill doesn't know what to do with it yet! Time to set up some email templates.

OrderCloud makes variables available to use in your Mandrill email templates. You can check out the full list [here][../merge-vars.md]. 

We also provide this repo of default email templates. These email templates have all been tested in the following email clients:
- Outlook
- Gmail
- iOS

However, when you make changes or if your clients use other email clients, we suggest testing your updated templates again. [Litmus](https://litmus.com/) is a great tool that we recommend.

### Put Default Templates Into Mandrill

You need a template for every message type that your message sender is configured for. Your templates must have the exact same name as the message type in OrderCloud.

1. Open your MailChimp account, and click on "Templates" in the top nav.
2. Click "Create Template", and "Code Your Own"
3. Copy/Paste into the MailChimp editor the exact code from the template in this repo. Remember to name the template exactly what the message config name is!
4. Save the template to MailChimp.
5. In the MailChimp template list, find the template you just made and select the dropdown arrow next to "Edit". Then click "Send to Mandrill".
6. If you log into Mandrill now, you will see the template you just made in Mandrill's template list. (Go to "Outbound", then "Templates") 
7. In our templates, we use the Handlebars merge language to tell Mandrill that our variables are variables, and that it shouldn't be rendered as plain text. However, Mandrill supports several merge languages, so you have to set the merge language. In Mandrill, go to "Settings", then "Sending Defaults", and set the Merge Language to "Handlebars", and save. 

## Send Emails!

You should now get emails for every configuration you set up!


For more information, check out our [blog post](https://ordercloud.io/transactional-emails-mandrill-ordercloud-io/), or ask us questions in our [OrderCloud Community Slack]().
