# My-Fruit-Diary

My Fruits Diary is a mobile application where you can store the number of fruits you have eaten each day. The user is able to add date entries and for each date choose the fruits eaten on that specific day. The application consumes a webservice where the current entries and fruits are located.

## Webservice 
- The available fruits are located at: GET [fruit](https://bit.ly/2MUkVls)
- The current entries are located at: GET [entry](https://bit.ly/2MzpmVR)
- To remove all current entries: DELETE [entries](https://bit.ly/2MzpmVR)

- Remove a specific entry: DELETE [/entryId](https://bit.ly/2wbBIsR)
- Parameter entryId: The id of an existing entry to remove.

-	Add an entry: 
			Content-Type: application/json	 
			POST [entry](https://bit.ly/2MzpmVR)			
      ```
			JSON Request Body: { "date": "2018-01-16"}
      ```
-	Set/edit a fruit:						
			  Content-Type: application/json 	
			  POST [entryId/fruitId/nrOfFruit](https://fruitdiary.test.themobilelife.com/api/entry/{entryId}/fruit/{fruitId}?amount={nrOfFruit})
        
 				Parameter entryId  :The id of the entry to add fruit to 	
 				Parameter fruitId  :The id of the fruit to be added to the entry	 
 				Parameter nrOfFruit :The number of fruit to be added to the entry

## Software Requirements

- **Requirement 1** The UI should at least have two tabs, ”My Diary” and ”About”.
- **Requirement 2** The existing entries should be presented through a list of some sort and a specific entry should be viewable through a detail view. Each row in the entries list should present the date of the entry, the number of fruits and the total number of vitamins in the eaten fruits that date.
- **Requirement 3** It should be possible to add and remove date entries.
- **Requirement 4** It should be possible the change/edit the different fruits and the number of fruits for each entry.
- **Requirement 5** The available fruits should be loaded during app start. They could be locally stored, but should be updated if the list of fruit changes on the server.
- **Requirement 6** The entries should not be locally stored other than in memory after reading from the back end.
- **Requirement 7** When adding a fruit to an entry, an image of the current fruit should be visible. The image can be cached.
- **Requirement 8** When adding a fruit to an entry the name of the fruit and the number of vitamins the fruit contains should be visible to the user.
