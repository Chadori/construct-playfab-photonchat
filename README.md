# construct-playfab-photonchat
The Script Interface documentation for the [Photon Chat](https://www.constructcollection.com/construct-playfab-photonchat) addon of the [Construct Master Collection](https://www.constructcollection.com/), for [Construct 3](https://www.construct.net/).

## IPhotonChat documentation
This is the documentation to use Construct 3's new JavaScript [Scripting feature](https://www.construct.net/en/make-games/manuals/construct-3/scripting/overview) with Photon Chat.

### Easy usage
You can easily access the PhotonChat object's interface using the `runtime`, from both the event sheet and script.
```JS
runtime.objects.PhotonChat.getFirstInstance().setAnimation("animationName", 0, 0);
```
For more information, please see the [scripting documentation of the Sprite object](https://www.construct.net/en/make-games/manuals/construct-3/scripting/scripting-reference/plugin-interfaces/sprite).

### Advanced usage
You can also subclass instances in a script, please see the [subclassing instances documentation](https://www.construct.net/en/make-games/manuals/construct-3/scripting/guides/subclassing-instances) for more information.
```JS
class Photon extends IPhotonChat
{
	constructor()
	{
		super();
	}
}
```

### API
The supported methods and properties to use in Construct 3's scripting feature with Photon Chat.

#### Globals
- Context - retrieve the current instance of the Photon Chat object.
- Client - retrieve the current instance's load balancing client.
- Photon - retrieve the global Photon object.

#### Actions
- setUserId (userId)
- setCustomAuthentication (authParameters, authType)
- setRegion (region)
- setAppId (appId)
- setAppVersion (version)
- connect ()
- disconnect ()
- subscribe (channelNames, historyLength, lastIds)
- unsubscribe (channelNames)  
- publishMessage (channelName, content)
- sendPrivateMessage (userId, content)
- addFriends (userIds)
- removeFriends (userIds)
- setUserStatus (statusOption, status, messageOption, statusMessage)
- reset ()
- PlayFabAuthenticate (PlayFabID, PhotonToken)
- GetPhotonAuthToken ()

#### Conditions
- isConnectedToNameServer ()
- isConnectedToFrontEnd ()

#### Expressions
- Result ()
- ErrorCode ()
- ErrorMessage ()
- State ()
- StateString ()
- UserId ()
- Channel ()	
- Message ()	
- Sender ()	
- UserStatusUserId ()	
- UserStatus ()	
- UserStatusString ()	
- UserStatusMessageUpdated ()	
- UserStatusMessage ()	
- ChannelLastMessageID (channelName)
- PhotonToken ()

### Guide
The API documentation only shows the **methods** with its **parameters**, sometimes this is not enough to fully understand each use of the references.
To solve that, use the **Photon Chat** addon as reference.

![image](https://user-images.githubusercontent.com/31282960/110241952-a8dbe900-7f8e-11eb-9117-94ff5104ad1a.png)

**Instructions**
- For **text** parameters, use `string` values.
- For **number** parameters, use `int` or `float` values.
- For **combo** parameters, use the placement of the drop-down selection, starting from `0`.
- For **toggle** parameters, use `boolean` values.
