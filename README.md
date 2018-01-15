Use Microsoft Azure AD v2 with Flask using `flask-oauthlib`.

This extends the [example provided by MS Azure](https://github.com/Azure-Samples/active-directory-python-flask-graphapi-web-v2) with full SSL enabled. SSL is *required* to use OAuth on non-localhost URLs. 

## Installation 

```
sudo pip install Flask flask-oauthlib
```

Register your Azure AD v2.0 app.  

- Navigate to the [App Registration Portal](https://identity.microsoft.com).
- Go to the the `My Apps` page, click `Add an App`, and name your app.  
- Set a platform by clicking `Add Platform`, select `Web`, and add a Redirect URI of ```https://localhost:5000/login/authorized```.
- Add ```https://your.site.url:5000/login/authorized```. 
- Click "Generate New Password' and record your Consumer Secret.  


Create self-signed cert:
```
openssl req \
       -newkey rsa:2048 -nodes -keyout key.key \
              -x509 -days 365 -out cert.crt
```

add your Application/Client ID and Consumer Secret to secrets.py.

```
$ python v2flaskapp.py 
```

## License.

This is based on: https://github.com/Azure-Samples/active-directory-python-flask-graphapi-web-v2

Copyright 2017, Microsoft. MIT License.

