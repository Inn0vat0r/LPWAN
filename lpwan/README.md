Directly leverage the power of IoT Central using the IoT Central device bridge. 
The device bridge connects other IoT clouds such as from Sigfox, Particle and The Things Network with IoT Central by forwarding the data devices send to the other clouds through to IoT Central app. 
In IoT Central app, build rules and run analytics on that data, create workflows in Microsoft Flow and Azure Logic apps, export that data.

The IoT Central device bridge is an open source solution in Github. 
https://aka.ms/iotcentralgithubdevicebridge

The resources include:

Azure Function app
Azure Storage account
App Service plan (S1 tier)
Azure Key Vault
The function app is the critical piece of the device bridge. It receives HTTP POST requests from other IoT platforms or any custom platforms via a simple webhook integration. We have provided examples that show how to connect to Sigfox, Particle, and TTN clouds. You can easily extend this solution to connect with your custom IoT cloud if your platform can send HTTP POST requests to your function app.

The function app transforms the data into a format accepted by IoT Central and forwards it along via DPS APIs.

