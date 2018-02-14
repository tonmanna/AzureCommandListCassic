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


Get-AzureReservedIPAssociation -ReservedIPName reservedIP -ServiceName “CloudService”  (this will list all the IP reserved by you) 

Remove-AzureReservedIPAssociation -ReservedIPName reservedIP -ServiceName “CloudService” (this will remove the reserve Ip from the VM) 

New-AzureReservedIP –ReservedIPName ReservedIP –Location “Location” -ServiceName  “CloudService” 

Set-AzureReservedIPAssociation -ReservedIPName reservedIP -ServiceName “CloudService”