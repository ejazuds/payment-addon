SAP Digital Payment Service Provider

Administration
 https://help.sap.com/docs/DIGITALPAYMENTS/a5c364402f8d4c0b99f6a4c7de385a56/f94d0c15b5c64349917ab8060c147ed0.html



Activating PSP  For the data center Europe (Frankfurt)
* Test account: https://<subdomain>.demo-digitalpayments-sap.cfapps.eu10.hana.ondemand.com/pspStatus/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu10.hana.ondemand.com/pspStatus/index.html
For the data center Europe (Frankfurt) EU Access
* Test account: https://<subdomain>.test-digitalpayments-sap.cfapps.eu11.hana.ondemand.com/pspStatus/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu11.hana.ondemand.com/pspStatus/index.html
For the data center US East (VA)
* Test account: https://<subdomain>.test-digitalpayments-sap.cfapps.us10.hana.ondemand.com/pspStatus/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.us10.hana.ondemand.com/pspStatus/index.html


Managing URLs on Allowlist

For security reasons, the SAP digital payments add-on will redirect only using known URLs.
To add an external redirect URL, access the Manage URLs on Allowlist UI using the URLs below, and provide the appropriate credentials.
Note
You will need to replace <subdomain> with the subdomain names you created earlier.
For the data center Europe (Frankfurt)
* Test account: https://<subdomain>.demo-digitalpayments-sap.cfapps.eu10.hana.ondemand.com/allowlistedURLs/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu10.hana.ondemand.com/allowlistedURLs/index.html
For the data center Europe (Frankfurt) EU Access
* Test account: https://<subdomain>.test-digitalpayments-sap.cfapps.eu11.hana.ondemand.com/allowlistedURLs/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu11.hana.ondemand.com/allowlistedURLs/index.html

PayPal

To set up the connection between the SAP digital payments add-on and PayPal, you use the PayPal Merchant Onboarding UI.
The URLs to access this UI have the following formats:
For the data center Europe (Frankfurt)
* Test account: https://<subdomain>.demo-digitalpayments-sap.cfapps.eu10.hana.ondemand.com/paypalOnboarding/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu10.hana.ondemand.com/paypalOnboarding/index.html
For the data center Europe (Frankfurt) EU Access
* Test account: https://<subdomain>.test-digitalpayments-sap.cfapps.eu11.hana.ondemand.com/paypalOnboarding/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.eu11.hana.ondemand.com/paypalOnboarding/index.html
For the data center US East (VA)
* Test account: https://<subdomain>.test-digitalpayments-sap.cfapps.us10.hana.ondemand.com/paypalOnboarding/index.html
* Productive account: https://<subdomain>.digitalpayments-sap.cfapps.us10.hana.ondemand.com/paypalOnboarding/index.html



Code PoC

https://github.com/christian-noack-diva-e/sap-digital-payments-poc


Blog Post

https://community.sap.com/t5/enterprise-resource-planning-blogs-by-members/how-to-integrate-sap-digital-payments-add-on-into-a-non-sap-e-commerce/ba-p/13552951


API in  Business Hub

https://api.sap.com/api/DPCoreAPI/resource/Payment_Card_Processes


chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/https://www.moneris.com/-/media/Files/Products/ERP-Support/ERPintegration_SAP_RefGuide-ENG.pdf


Setup

https://help.sap.com/docs/DIGITALPAYMENTS/a5c364402f8d4c0b99f6a4c7de385a56/4a9bd0ded8534702b73002c9e89b45a1.html


https://help.sap.com/docs/subscription-billing/integration/integration-with-sap-digital-payments-add-on

https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/9442486404b54071b4ebeab6a16628e7/2ae5161d164341ffa3d197795237fca4.html

https://community.sap.com/t5/financial-management-blogs-by-sap/out-of-the-box-integration-for-credit-card-payments-in-s-4hana/bc-p/13438659


{
    "PaymentMethods": [
        {
            "Code": "EP",
            "Descriptions": [
                {
                    "Language": "en",
                    "Description": "External Payment"
                }
            ]
        },
        {
            "Code": "CC",
            "Descriptions": [
                {
                    "Language": "en",
                    "Description": "Credit Card"
                }
            ]
        }
    ],
    "PaymentServiceProviders": [
        {
            "Code": "DPDU",
            "Description": "Adapter for Dummy Payment Service",
            "PaymentMethods": [
                {
                    "Code": "CC",
                    "Descriptions": []
                },
                {
                    "Code": "EP",
                    "Descriptions": []
                },
                {
                    "Code": "PO",
                    "Descriptions": []
                }
            ]
        },
        {
            "Code": "DPPP",
            "Description": "PayPal",
            "PaymentMethods": [
                {
                    "Code": "EP",
                    "Descriptions": []
                }
            ]
        }
    ]
}





