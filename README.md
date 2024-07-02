Very short info:
- Check your localStorage for a field named token on the Escapade page
- The endpoint you want to connect to is: wss://escapade.fun:2053/ws 
- This is a websocket endpoint, so use a websocket library.
- Data serialization / deserialization is done using protobuf.
- You will need to compile the protocol to the language of your choice.

- Atart your connection with a JoinWorld message 
- All messages you'll receive and send thereafter will be of type WorldEvent 
- You don't have to set the issuer_local_player_id  when sending a message 
- Send a WorldEvent message with event_type  WorldEventType.Sync if you want to make the bot visible in the game 
