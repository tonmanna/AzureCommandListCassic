#Login 

ADD-AzureAccount   #Login with your azure credentials

#Select Subscription ID

Select-AzureSubscription –SubscriptionId ‘cxSubID’

#Create with Add to cloud Service

New-AzureReservedIP –ReservedIPName ReservedIP –Location “Location” -ServiceName  “CloudService”

#Update Current active cloud service

Set-AzureReservedIPAssociation -ReservedIPName reservedIP -ServiceName “CloudService”

#Remove reserved IP from cloud service

Remove-AzureReservedIPAssociation -ServiceName "“CloudService”"