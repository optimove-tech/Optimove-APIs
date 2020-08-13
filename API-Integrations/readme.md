## Integrate Your Service with Optimove - Best Practices

- [Pre-scheduled Flow](#pre-flow)
- [Realtime Flow](#rt-flow)
- [Bonus Integration Flow](#bonus)
<br/>

### <a id="pre-flow"></a>Pre-Scheduled Flow: 
**Use Cases**: 

 1. As an Optimove client, you wish to integrate to an external service with Optimove and act as the middle-ware.
 2. As a third party vendor / partner, you are interested in using Optimove to automatically send customer campaigns via your marketing platform.

<p align="center"><img src="https://github.com/optimove-tech/Optimove-APIs/blob/master/API-Integrations/Integrate%20Your%20Service%20-%20Pre-Scheduled%20-%20Client%20Execution%20Flow.png?raw=true"></p>

>**Notes**: 
> -   For API Authentication (#1 above) best practice refer to -   [Login API best practice & use cases](https://github.com/optimoveproductintegration/Optimove-APIs/tree/master/Login-API)
> -   For EventTypes (#2 above) refer to [RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener)
> -   Please contact the Product Integration Team to provide you with the exact Channel ID you should register the listener ([RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener)), and synchronize your templates to ([AddChannelTemplates](https://docs.optimove.com/api-usage-guide/#AddChannelTemplates) #3 above)
> -  For more details, please refer to our [Optimove docs site](https://docs.optimove.com/integrate-your-service-with-optimove/)
<br/>

----------
### <a id="rt-flow"></a>Realtime Flow: 
**Use Cases**: 

1. As an Optimove client, you wish to automatically send your customers realtime campaigns based on Optimove's [Track & Trigger](https://docs.optimove.com/track-and-trigger/) add-on product.
 2. As a third party vendor / partner, you are interested in using Optimove to automatically send customer realtime campaigns based on Optimove's [Track & Trigger](https://docs.optimove.com/track-and-trigger/) add-on product enabled in your client's Website / Mobile Application via your marketing platform.

<p align="center"><img src="https://github.com/optimove-tech/Optimove-APIs/blob/master/API-Integrations/Integrate%20Your%20Service%20-%20Realtime%20-%20Client%20Execution%20Flow.png?raw=true"></p>

>**Notes**: 
> - This integration flow **supports** Optimove clients who have Optimove's [Server Side API](https://github.com/optimove-tech/Reporting-Server-Side-Custom-Events) or[Track & Trigger](https://docs.optimove.com/track-and-trigger/) add-on product running on their website, mobile native app **only**!
> -   For API Authentication (#1 above) best practice refer to -   [Login API best practice & use cases](https://github.com/optimoveproductintegration/Optimove-APIs/tree/master/Login-API)
> - The API payload you will receive in realtime is described in [RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener) under EventTypeID = 11
> -   Please contact the Product Integration Team to provide you with the exact Channel ID you should register the realtime listener ([RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener)), and synchronize your templates to ([AddChannelTemplates](https://docs.optimove.com/api-usage-guide/#AddChannelTemplates) #3 above)
> -  For more details, please refer to our [Optimove docs site](https://docs.optimove.com/integrate-your-service-with-optimove/)
<br/>

----------
### <a id="bonus"></a>Bonus Integration Flow: 
**Use Cases**:

1.  As an Optimove client, you wish to integrate Optimove with your promo/bonus system.
2.  As a third party vendor / middle-ware provider, you are interested in integrating a promo/bonus system with Optimove and allow Optimove clients to manage customer campaigns that also automatically grant bonuses, discounts, incentives, etc. to individual customers.
<p align="center"><img src="https://github.com/optimove-tech/Optimove-APIs/blob/master/API-Integrations/Integrate%20Your%20Service%20-Bonus%20System%20Event13.png?raw=true"></p>

>**Notes**: 
> -   For API Authentication (#1 above) best practice refer to -   [Login API best practice & use cases](https://github.com/optimoveproductintegration/Optimove-APIs/tree/master/Login-API)
> -   For EventTypes (#2 above) refer to [RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener)
> -   Please contact the Product Integration Team to provide you with the exact Channel ID(s) you should register the listener ([RegisterEventListener](https://docs.optimove.com/api-usage-guide/#General_Functions_RegisterEventListener)) 
> - In order to have the promotions available for choosing within the campaign creation, please use [Add Promotions](https://docs.optimove.com/api-usage-guide/#External_System_Integration_Functions_AddPromotions)
>  - Once a notification to your listener is received for EventTypeID13,  pull the relevant details of the campaign using **both the CampaignID and ChannelID** received within the notification (#6 and #9 above). ([GetCustomerExecutionDetailsByCampaign](https://docs.optimove.com/api-usage-guide/#GetCustomerExecutionDetailsByCampaign) 
>  - For **multi-channel** campaigns, in order to avoid granting the promotion twice to the same user within the same campaign, filter the users across the different channels (#7 and #10 above).
>  -  For more details, please refer to our [Optimove docs site](https://docs.optimove.com/integrate-your-service-with-optimove/)
