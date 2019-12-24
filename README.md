# Resources

[Filling in blank form data](https://stackoverflow.com/questions/26764197/how-to-empty-a-numeric-value-from-a-form-built-with-wtform)

[Getting form data](https://stackoverflow.com/questions/10434599/get-the-data-received-in-a-flask-request)

[Form submit is always false - FIX](https://stackoverflow.com/questions/20905188/flask-wtforms-validation-always-false)

[Form submit is always false - PART TWO](https://stackoverflow.com/questions/20905188/flask-wtforms-validation-always-false)

^ This can also be fixed by not filling in the StringFields with empty strings

[Base template for this web application](https://www.youtube.com/watch?v=UIJKdCIEXUQ)

[Flask Application to get Spotify Web Authentication](https://stackoverflow.com/questions/26726165/python-spotify-oauth-flow)

^ This code is paramount to the entirity of this project

[Initialize Spotify Driver without reading from environment variables](https://sotiriskakanos.com/2017/08/05/using-spotifys-web-api-with-python/)

[Decode urls](https://www.urldecoder.org/)

[Analyzing my Spotify Music Library](https://vsupalov.com/analyze-spotify-music-library-with-jupyter-pandas/)

[Using Flask inside a Python Class](https://stackoverflow.com/questions/40460846/using-flask-inside-class)

[Explaining Python decorators](https://gist.github.com/Zearin/2f40b7b9cfc51132851a)

# Working in the command line

Each project folder is like a Git repository and has access to certain tools only in an initialized elastic beanstalk repo
- make a project folder by typing: `eb init --interactive`. If `eb init` is used, some errors occur and will not allow you to proceed
- credentials for `eb init` can be found in the online portal by following [this link](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html)
- this is how the access keys work : [link to documentation](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys)
- Deploy using `eb deploy` in the project folder
- Open the project in a web browser by typing `eb open`


[Install eb](https://github.com/aws/aws-elastic-beanstalk-cli-setup)


# Documentation

## Scopes

These are the permissions that you, the end user grant this program.
The term "scope" refers to how much funnel cake can see in your Spotify account.

### playlist-modify-public

This allows for cleaning the newly create playlist. Truncating was a feature introduced in the command line version but has since seen no real use in AWS version (web application).

### user-private-read

Makes sure the playlist being created does not already exist and we need to list the user's playlists for this validation process.

### user-library-modify

Allows for the creation of playlists on a user's account.

### user-read-email and user-read-private

Needed to get the current user's id and account name. This is used to create playlists and to display who has been logged in.

### External Documentation

You can read more about the other types of scopes that can be used [here](https://developer.spotify.com/documentation/general/guides/scopes/).
