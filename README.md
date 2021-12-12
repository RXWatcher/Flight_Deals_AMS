# Flight_Deals_AMS
Project for viewing the cheapest flight deals from Netherlands to other countries.

Sample sheet = https://docs.google.com/spreadsheets/d/1L5dLuKqe2JLCVsnpOSp6E50R6OUXWRUILcfyfzMYA1s/edit?usp=sharing
The sheet should have at least the name of the city and the min price (I took some big number e.g. 100000 at first)

In oder to use it, need to set up sheety.co, bit.ly and tequila-api.kiwi.com accounts at least (twilio is optional, can be commented along with send_email function call if you don't want to be notified).

1) For sheety.co configuration you need to change "SHEET_ENDPOINT" var as well as add you own sheet to your account and enable "GET", "POST", "PUT".
2) Bit.ly requires 'BITLY_TOKEN', which you can get after signing up.
3) For tequila.kiwi.com you'll need API_KEY which you can get after signing up and registring an application.

On the first run it will get IATA codes for all rows if it's not there.
On the second run it will find the best flights starting from tomorrow up to 6 months. It will try to find direct flight first and then will keep increasing the number of stop overs until it finds something or there will be too many stops (default = 3).
Parameter can be configured under flight_search.py search_flight function inside 'payload' var.
