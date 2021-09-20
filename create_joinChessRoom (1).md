# Create a New Game

- Method: Post
- Description: Create a new game

#### If the number of ongoing games is less than 6, a new game room with a unique ID is created. There can’t be more than 6 games running concurrently. This also restarts a completed game.
##### REQUEST BODY SCHEMA: application/json


##### Required parameters;
| Name | Data type |
| ------ | ------ |
| User_ID | integer |
| User_name | string |
| User_ID | string |


> Once you click on Join as player 1, all parameters will be inputed automatically, then you recieve a response.

### Responses with description
``` sh
Code: 200
Description: Success, return ID of created game


Code: 500
Description: Internal server error
{
  "message": "Unable to Create a Game: CustomError: Unable to Connect to Zuri Core DB [UPDATE]: Error: Request failed with status code 500",
  "data": null,
  "success": false
}
```
##### Url link [https://chess.zuri.chat/api/v1/game/create]




# Join a Game

- Method: Post
- Description: Enter a game as the second player

#### After a game is created, you can join as the second party to play against the creator. 
##### REQUEST BODY SCHEMA: application/json


##### Required parameters;
| Name | Data type |
| ------ | ------ |
| game_ID | string |
| User_ID | integer |
| User_name | string |
| User_ID | string |


> Once you click on Join as player 2, all parameters will be inputed automatically, then you recieve a response.

### Responses with description
``` sh
Code: 200
Description: Success, joined a created game


Code: 500
Description: Internal server error
{
  "message": "Unable to Create a Game: CustomError: Unable to Connect to Zuri Core DB [UPDATE]: Error: Request failed with status code 500",
  "data": null,
  "success": false
}
```
##### Url link [https://chess.zuri.chat/api/v1/game/join]


