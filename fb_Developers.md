- Unordered list can use asterisks

* Create an app in developer.facebook.com
* Take app secret from settings -> Basic
* Click on add icon next to products title and then follow the next steps
  1. Click on setup in webhooks card.
  2. Select page option from drop down and click on subscribe to object button
  3. Fill the url with endpoint you created with fb webhook code.(It should be a public endpoint with https, you can host with ngrok)
  4. Fill verify token you have used in webhook code
  5. Click on save and if its verified successfully , it will go back to previous screen
* Again click on add icon again
  1. click on setup in messenger card
  2. click on Add or remove pages button
  3. Accept all the permissions
  4. Page will be added to list.
  5. Click on add subsciptions button
  6. Check the items (messages,message_postbacks, handover,standby)
  7. Click on Generate token in Messenger -> settings -> Access tokens
  8. Copy the token to your webhook code.
