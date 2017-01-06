# PiOrder
Raspberry Pi & Pipsta based restaurant [Point of Sale](https://en.wikipedia.org/wiki/Point_of_sale#Hospitality_industry), Ticketing &amp; Online Ordering.

## Images

At the restaurant:

![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/image2.JPG)

![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/image3.JPG)

![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/image4.JPG)

Mobile ordering:

![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/IMG_1979.PNG)
![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/IMG_1980.PNG)
![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/IMG_1982.PNG)
![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/IMG_1983.PNG)

## Video 
(Video to be completed)

## Live Online Demo

Live near Kingswood, Surrey? [Order online!](https://khybertandoori.com/order/login)
NB: Not accessible outside the UK


### Topology
![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Images/Topology.png)

##Features
1. Orders using a touch based POS by waiters. 
2. Print bar receipts and order tickets to the kitchen. 
3. Allow customers to order online.
4. View the bar or kitchen using RP cameras.

##Technical Overview
   * A Raspberry Pi webserver is used to implement the POS (JavaScript/JQuery/PHP).
   * The Pipsta printers are used to print the customer receipts or kitchen tickets (Python, Bash Scripts, SCP).
   * Orders arriving from a website are sent to the bar and kitchen for printing (SCP).
   * The website creation is agnostic, but we've used Symfony2 & PHP. Bash, Awk and Cron used for handling of the orders and current waiting time.
   * No central database is used - using files is sufficient.

### Hardware
1. 2 x [RP Model 2B](https://www.raspberrypi.org/products/raspberry-pi-2-model-b)
2. 2 x [Pipsta](http://www.pipsta.co.uk)
3. 1 x Web Hosting ([we use 4uhosting.co.uk](https://www.4uhosting.co.uk))
4. 1 x Wifi router & internet connection
5. 1 x Pair of powerline ethernet adaptors
6. 1 (or more) Tablets (for web browsing)
7. Optional: Raspberry Pi Cameras

#FAQ's
Q: Why print onto paper / why not go fully electronic?
A: For customers, a paper receipt is still common. For chefs in the kitchen, paper has value in a kitchen environment. [An interesting discussion here](http://www.cheftalk.com/t/69312/for-those-in-professional-kitchens-ticket-taking-expediting).

Q: How much does this cost roughly?
A: Approx £545 for the hardware, then £65/year for Web Hosting (host, domain and SSL certificate), £50/year for thermal papers and £30/month for Telehphone & Internet. The internet can of course be shared with customers as a service.

| Item            | Cost           | 
| --------------- | --------------:|
|1 Large Tablet   |            £130|
|2 Small Tablets  |            £100|
|1 Wireless router|             £30|
|1 Printer Cam    |             £20|
|2 Raspberry Pi's |             £70|	
|2 Pipista Printers|           £140|	
|Socket Ethernet  |	            £50|	
|Ethernet cables  |              £5|	
|Thermal paper    |        £50/year|
|Web Hosting      |        £65/year|
|Internet & Telephone|    £30/month|

Q: How reliable are the Pipsta printers, Raspberry Pi's and tablets? 
A: We've been running all the above for a full year with no hardware based problems.

Q: Which tablets are you using?
A: Amazon Kindle Fires (2 x 7 inch and 1 x 10.1 inch)
