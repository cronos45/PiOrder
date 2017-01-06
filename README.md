# PiOrder
Raspberry Pi & Pipsta based EPOS, Restaurant Ticketing &amp; Online Ordering.

##Features
1. Handling of all orders using a touch based EPOS by waiters. 
   * No manual writing, illegibility or tallying!
2. Printing of kitchen tickets at the bar or kitchen within, multiple times for different chefs. 
   * No carbon copy requiring walking! 
   * We also a camera to physically see the kitchen printout
   * We play a sound for the chefs to hear the order arrival.
3. View how busy the kitchen is from using other Raspberry Pi cameras. Important for knowing the currentwaiting time for orders.
4. Allow customers to order online
   * Waiting time can set by waiters via the tablets and/or scheduled. Hangryness should not be underestimated (customers can get very angry if they are hungry and their order is late).
   * Orders arrive straight to the bar and kitchen printers. 
   * Frees up waiters manually taking a telephone order. 
   * Receipts are emailed to the customers.

##Technical Overview
A Raspberry Pi webserver is used to implement an EPOS (JavaScript/Jquery/PHP).

The Pipsta printers are used to print the customer receipts or kitchen tickets (Python, Bash Scripts, SCP).

Orders arriving from a website are sent to the bar and kitchen for printing (SCP).

The website creation is agnostic, but we've used Symfony2 & PHP. Bash, Awk and Cron used for handling of the orders and current waiting time.

No central database is used - using files is sufficient for this system.

### Hardware
1. [RP Model 2B](https://www.raspberrypi.org/products/raspberry-pi-2-model-b)
2. [Pipsta](http://www.pipsta.co.uk)
3. Web Hosting ([we use 4uhosting.co.uk](https://www.4uhosting.co.uk))
4. Wifi router & internet connection
5. Socket ethernet
6. Tablets (or any web browser)

### Topology
![ScreenShot](https://github.com/EMRahman/PiOrder/blob/master/Topology.png)
