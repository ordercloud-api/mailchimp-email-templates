# Available Mandrill Template Merge Vars (as of June 15, 2017)

## Password Reset Emails

|         mergeVar        |                         OrderCloud Equivalent                          |
|-------------------------|------------------------------------------------------------------------|
| username                | username                                                               |
| password token          | passwordtoken                                                          |
| password verification   | passwordverificationcode                                               |
| password renewal url    | passwordrenewalurl                                                     |



## Order Emails 

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
|-------------------------|------------------------------------------------------------------------|
| Vars below only avx on  |                                                                        |
| Order Shipment Emails   |                                                                        |
|-------------------------|------------------------------------------------------------------------|
| ShipmentID              | Shipment.ID                                                            |
| ShipmentTrackingNumber  | Shipment.TrackingNumber                                                |
| Shipper                 | Shipment.Shipper                                                       |
| dateShipped             | Shipment.DateShipped                                                   |
| toAddressID             | Shipment.ToAddress.ID                                                  |
| toAddressCompany        | Shipment.ToAddress.Company                                             |
| toAddressFirstName      | Shipment.ToAddress.FirstName                                           |
| toAddressLastName       | Shipment.ToAddress.LastName                                            |
| toAddressStreet1        | Shipment.ToAddress.Street1                                             |
| toAddressStreet2        | Shipment.ToAddress.Street2                                             |
| toAddressCity           | Shipment.ToAddress.City                                                |
| toAddressState          | Shipment.ToAddress.State                                               |
| toAddressPostalCode     | Shipment.ToAddress.PostalCode                                          |
| toAddressCountry        | Shipment.ToAddress.Country                                             |
| toAddressName           | Shipment.ToAddress.AddressName                                         |
|-------------------------|------------------------------------------------------------------------|
| shipmentItems (array)   |                                                                        |
|-------------------------|------------------------------------------------------------------------|
| Cost                    | LineItem.LineTotal                                                     |
| QuantityShipped         | Shipment.Item.QuantityShipped                                          |
| ProductDesc             | Shipment.Item.Product.Description                                      |
| ProductID               | Shipment.Item.Product.ID                                               |
| ProductName             | Shipment.Item.Product.Name                                             |
|-------------------------|------------------------------------------------------------------------|


