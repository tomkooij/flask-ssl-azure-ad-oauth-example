## Installation 

```
sudo pip install Flask flask-oauthlib flask-sslify
```

Register your Azure AD v2.0 app.  
    - Navigate to the [App Registration Portal](https://identity.microsoft.com). 
    - Go to the the `My Apps` page, click `Add an App`, and name your app.  
    - Set a platform by clicking `Add Platform`, select `Web`, and add a Redirect URI of ```https://localhost:5000/login/authorized```.
    - Add ```https://your.site.url:5000/login/authorized```. 
    - Click "Generate New Password' and record your Consumer Secret.  


add your Application/Client ID and Consumer Secret to secrets.py.


```
$ python v2flaskapp.py 
```

