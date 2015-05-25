ebay2diamond
============

Simple php script to convert an eBay exported CSV to a Diamond Logistics compatible import CSV. 

This script: 
  * Prompts the user to combine multiple orders into a single parcel
  * Prompts the user for weights for each parcel
  * Handles the weird eBay export of multi-purchase orders (if the user orders >1 item in a single basket)
  * Imports the correct email (for tracking)
  * Uses eBay order reference number(s) to be printed on the label. 
  * Processes orders in the same order as the eBay sales page or printed manifest (no more ordering by postcode!)
  * Handles splitting of names into forename(s) / surname.
  * Handles ebay CSV sanitising

It does NOT:

  * Allow you to specify number of parcels - one per processed order is presumed
  * Allow you to specify delivery instructions - doesn't appear in the eBay CSV, you have to fill this in on DL website
    
To use:
  * Download your sales data from eBay
  * Place file in same folder as this script
  * run 'php ebay2hermes.php -f yourfilename.csv'

Works fine on windows but does not produce colored output for error messages - read carefully.
