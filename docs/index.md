# Welcome to Lightspeed Retail integration with Magento 2.

This guide has been written for the integration vendor name: maurisource/lightspeed only available from [Magento Commerce](https://marketplace.magento.com/maurisource-lightspeed.html) and [Maurisource Store](https://store.maurisource.com/)
Redacted for version 1.3.62 of the integration module.

### Omnichannel environment and source logic

The integration between Lightspeed Retail POS and Magento unlocks an omnichannel environment.
Source Inventory is Lightspeed Retail >> Which means: Magento's product catalog is populated from Lightspeed Items.
Source code is not available via GitHub as per vendor's distribution license.

**Schema** of the default business logic workflow implemented:
![lightspeed-Magento-integration-Scenario-design-visual-updated](https://user-images.githubusercontent.com/1178609/107824051-cd0d2700-6d4e-11eb-8754-cbae750c74aa.png)



### Integration Approved by: Lightspeed Retail and Magento Marketplace
**Lightspeed Retail** checks API level requests, checks for leaky bucket implementation, load relationship, orders creation, continuous stress on system. Partnership established allows each API Key to have their full API request allowance for maximum performance out of the box.
**Magento Commerce** run through an elaborate panel of automated technical tests and manual test. M2EQ test, MFTF, Code Sniffer, Semantic Check, Installation and Varnish test.

Although the integration utilizes data transmission SHA256, information trasmission goes directly from the Merchant's store >> Lightspeed Retail.
There is no middleware interception, hence eliminating all risks of sensible order info or product info.
There is an API Key service running within the application, which pings our server in order to refresh it's last cached token and provide a new one on request.

## Automation
Automation sync runs via CRON Schedule as per Magento's default cron:setup command.

## Syncing logic explained

## Compatibility
**stable**
Magento-ce 2.2.x 
Magento-ce 2.3.x
Magento-ee 2.2.x
Magento-ee 2.3.x

**alpha**
Magento-ce 2.4.x
Magento-ee 2.4.x

# @ToDo to be redacted for this guide
- Add product image banner
- Product demonstration video
- Installation using Composer
- CRON setup
- API Key authentication and cache
- Attributes mapping
- Syncing tags
- Syncing manufacturers (Lightspeed Vendors)
- Syncing orders
- Manual force sync methods (admin and CLI tool)
- SMART HASH system

### Major confirmed features added to road map
- Add stable compatibility with PHP 7.4.0
- Add stable compatibility with Magento Commerce 2.4.x
- Add support for MSI (Multi Source Inventory) distributed under maurisource/lightspeed v.1.4.0 

### Unconfirmed business logic ideas
- Add possibility for admin to disable some fields from sync.
- Add possibility for admin to change their attributes mapping.
- Add possibility for admin to add new attributes to the sync.

### Module distribution channel for full transition towards composer
Considering an option to distribute package via Composer for versions distributed outside of Magento Repository. (Currently checking GitLab public packages)

### Support or Contact

Check out our current [documentation](https://docs.google.com/document/d/1jVT4F1kaO88IxRQ1orJS7SlFdMveVzRCxK0xpQrLZZs/edit#) or [contact support](https://maurisource.zendesk.com/hc/en-us/requests/new) and we’ll help you sort it out.
