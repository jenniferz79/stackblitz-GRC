# stackblitz-GRC

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/web-platform-yf8ehx)

[Web URL](https://web-platform-yf8ehx.stackblitz.io)

# Google reCAPTCHA
## v2 I am not a robot
* User needs to tick the box, either get the green tick, or asked to do puzzle selection until pass
* Application need to get the token and send API request to [verify the response](https://developers.google.com/recaptcha/docs/verify)
* Can be disabled for automation testing purpose using generic site key and site secret
```
   Site key: 6LeIxAcTAAAAAJcZVRqyHh71UMIEGNQ_MXjiZKhI
   Secret key: 6LeIxAcTAAAAAGG-vFI1TnRWxMZNFuojJ4WifJWe
```

![Screenshot 2023-04-27 at 2 55 25 PM](https://user-images.githubusercontent.com/58871282/234747972-aad87276-4849-4931-bfd6-232a4151eb51.png)

## v2 invisible
* User does not need to tick any box.
* When click the button, it might be asked to solve puzzle if GRC suspects it is a bot
* Application need to get the token and send API request to [verify the response](https://developers.google.com/recaptcha/docs/verify)
* Can be disabled for automation testing purpose using generic site key and site secret as above

![Screenshot 2023-04-27 at 2 59 49 PM](https://user-images.githubusercontent.com/58871282/234748565-9d61e93f-ca22-4457-9cf6-954e383aa8aa.png)

## v3
* Truely invisible, user does not need to do any puzzle.
* Application need to get the token and send API request to [verify the response](https://developers.google.com/recaptcha/docs/verify), and get the response with score
```
    {
    "success": true,
    "challenge_ts": "2023-04-27T02:23:09Z",
    "hostname": "web-platform-yf8ehx.stackblitz.io",
    "score": 0.9,
    "action": "forgotPassword"
    }
```
* Application needs to take action for score as bot (0-0.4).
 


