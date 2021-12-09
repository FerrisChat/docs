# Messages

A Message object is structured as follows:

| Name       | Type                       | Description                                                                                                                   |
|------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| id         | u128                       | message id                                                                                                                    |
| content    | String                     | message content                                                                                                               |
| channel    | Channel                    | message channel's object                                                                                                      |
| channel_id | u128                       | message channel's id                                                                                                          |
| author_id  | u128                       | message author's id                                                                                                           |
| author     | Option\<User>              | author of this message                                                                                                        |
| edited_at  | Option\<PrimitiveDateTime> | the last time this message was edited                                                                                         |
| embeds     | Vec\<Embed>                | a list of embeds in this message                                                                                              |
| nonce      | Option\<String>            | nonce of this message: is not stored in DB so is none everywhere except for the WebSocket event and returned object from HTTP |
