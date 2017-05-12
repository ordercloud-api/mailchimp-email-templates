# Mailchimp Email Templates from OrderCloud.io

[Read the blog post!](https://ordercloud.io/transactional-emails-mandrill-ordercloud-io/)

## Avalible Mandril Template Merge Vars (as of January 6th, 2017)

### Password Reset Emails
- username
- passwordtoken
- passwordrenewalurl

### Order Emails 

|         mergeVar        |                         OrderCloud Equivalent                          |
|-------------------------|------------------------------------------------------------------------|
| firstname               | Order.FromUser.FirstName                                               |
| lastname                | Order.FromUser.LastName                                                |
| orderid                 | Order.ID                                                               |
| datesubmitted           | Order.DateSubmitted                                                    |
| subtotal                | Order.Subtotal                                                         |
| tax                     | Order.TaxCost                                                          |
| shippping               | Order.ShippingCost                                                     |
| total                   | Order.Total                                                            |
| lineitemcount           | Order.LineItemCount                                                    |
|-------------------------|------------------------------------------------------------------------|
| products (array)        |                                                                        |
|-------------------------|------------------------------------------------------------------------|
| Cost                    | LineItem.LineTotal                                                     |
| Quantity                | LineItem.Quantity                                                      |
| ProductDesc             | Product.Description                                                    |
| ProductID               | Product.ID                                                             |
| ProductName             | Product.Name                                                           |
| ShipToName              | LineItem.ShippingAddress.FirstName + LineItem.ShippingAddress.LastName |
| ShipToStreet1           | LineItem.ShippingAddress.Street1                                       |
| ShipToStreet2           | LineItem.ShippingAddress.Street2                                       |
| ShipToCity              | LineItem.ShippingAddress.City                                          |
| ShipToState             | LineItem.ShippingAddress.State                                         |
| ShipToPostalCode        | LineItem.ShippingAddress.Zip                                           |
| ShipToCountry           | LineItem.ShippingAddress.Country                                       |
|-------------------------|------------------------------------------------------------------------|
| approvals (array)       |                                                                        |
|-------------------------|------------------------------------------------------------------------|
| ApprovingGroupID        | Order.Approval.ApprovingGroupID                                        |
| Status                  | Order.Approval.Status                                                  |
| DateCreated             | Order.Approval.DateCreated                                             |
| DateCompleted           | Order.Approval.DateCompleted                                           |
| ApproverID              | Order.Approval.Approver.ID                                             |
| ApproverEmail           | Order.Approval.Approver.Email                                          |
| ApproverFirstName       | Order.Approval.Approver.FirstName                                      |
| ApproverLastName        | Order.Approval.Approver.LastName                                       |
| ApproverUsername        | Order.Approval.Approver.Username                                       |
| ApproverPhone           | Order.Approval.Approver.Phone                                          |
|-------------------------|------------------------------------------------------------------------|
| orderxp (array)         |                                                                        |
|-------------------------|------------------------------------------------------------------------|
| orderxp_KeyName         | For basic xp objects                                                   |
| orderxp_KeyName_KeyName | For nested xp objects                                                  |
| orderxp_KeyName_Index   | For xp arrays                                                          |
