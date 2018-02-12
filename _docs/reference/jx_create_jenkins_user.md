## jx create jenkins user

Adds a new user name and api token for a jenkins server server

### Synopsis


Creates a new user and API Token for the current Jenkins Server

```
jx create jenkins user [username]
```

### Examples

```
  # Add a new API Token for a user for the current Jenkins server
  # prompting the user to find and enter the API Token
  jx create jenkins token someUserName
  
  # Add a new API Token for a user for the current Jenkins server
  # using browser automation to login to the git server
  # with the username an password to find the API Token
  jx create jenkins token -p somePassword someUserName
```

### Options

```
  -t, --api-token string   The API Token for the user
  -b, --batch-mode         In batch mode the command never prompts for user input
      --headless           Enable headless operation if using browser automation
  -n, --name string        The name of the git server to add a user
  -p, --password string    The User password to try automatically create a new API Token
      --timeout string     The timeout if using browser automation to generate the API token (by passing username and password)
  -u, --url string         The URL of the git server to add a user
      --verbose            Enable verbose logging
```

### SEE ALSO
* [jx create jenkins](jx_create_jenkins.md)	 - Creates a jenkins resource

###### Auto generated by spf13/cobra on 12-Feb-2018