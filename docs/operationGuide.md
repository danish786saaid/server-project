# Operation Guide

> [!NOTE]
> To test the CURL Commands, replace the url either with the live demo url, or your self host one.

## Login

![login.png](img/login.png)
To login,
1. Enter both your email and password.
2. Click "Login". (Send POST request `/api/login`)

## Case
### Vaild input
Using correct credentials to log in

| email | password |
| --- | --- |
| test@example.com | 1234 |

Result: User successfully authenticated and will be redirected to the home page

### Invalid input
Using incorrect credentials to log in / wrong email format

Result: Error message will be displayed

![login-failed.png](img/Invalidinput1.png)
![login-failed.png](img/Invalidinput2.png)

## Signup

![signUp.png](img/signUp.png)

To create you account,
1. Enter your Name, Email, password, and the confirm password to double check the password.
2. Click "Sign up". (Send POST request `/api/signup`)
3. If the password matched and the user name is available, the system will save the registered user information to the database
4. Redirect to the home page

## Case
### Vaild input

| field            | value                |
|------------------|----------------------|
| Username         | Chung    |
| Email            | Chung@example.com |
| Password         | Chung123          |
| Confirm Password | Chung123          |

Result: User is successfully registered and will be redirected to the home page

### Invalid input
Username or email already exists / password does not match / Missing any field


![signUp-failed1.png](img/signUp-failed1.png)


Result: Error message will be displayed


### Google OAuth

Uses post request `/auth/google` to login / register with Google OAuth

To sign in / sign up with Google OAuth,
1. Click either "Continue with Google" or "Register with Google", depending on which page you are in
2. Choose the account / Login to your Google account
3. Authorize the application to fetch your information

If authentication is successful, the system will redirect to the home page.
If failed to authenticate, the system will redirect to the login page

# Home

Test using CURL
READ
```text
curl -X GET "https://server-project-14rn.onrender.com/api/notes"
## Create note
```

![Create-Note.png](img/Create-Note.png)

To create a note,
1. Click the "Create Note" Input box
2. Write something in the input box
3. Click the "Add note" button (Send POST request `/api/note`))
4. Wait the server to acknowledge and display a new card with the written content onto the page

Test using CURL

CREATE
```text
curl -X POST "https://server-project-14rn.onrender.com/api/notes" ^
  -H "Content-Type: application/json" ^
  -d "{\"noteContent\":\"New Note\"}"
```

## Edit note

To edit a note,
1. Click on the content on the note card
2. Edit the content by typing it, changes will be saved automatically (Send PUT request `/api/note/:id`) with interval of 5 seconds when focus
3. When the content lost focus, the changes will be saved to the database

Test using CURL

```text
curl -X PUT "https://server-project-14rn.onrender.com/api/notes/6925488b15b25d690ebd64a1" ^
  -H "Content-Type: application/json" ^
  -d "{\"noteContent\":\"Updated Note\"}"
```

## Delete note
To delete a note,
1. On the note that would like to delete, click the "Delete" icon button
2. Click "Delete" to confirm the deletion
3. Send DELETE request `/api/note/:id` to server to execute the delete action
4. When the action is completed, the note will be removed from the page

Test using CURL

```text
curl -X DELETE "https://server-project-14rn.onrender.com/api/notes/6925488b15b25d690ebd64a1"
```

## Search note
To search for a note,
1. Click the "Search" Input box
2. Write something in the input box
3. The POST request `/api/search` will be sent along with the keyword to the server when user stop typing
4. Wait the server to acknowledge and query the result

If result is found, the system will display the result on the page
If result is not found, the system will display a message that there are no matching results
If the keyword is empty, the page will show all the note entry

Test using CURL
```text
curl -X POST http://your-api-url/api/searchNotes \
-H "Content-Type: application/json" \
-d '{"keyword": "your_search_keyword"}'
```
![showcase.png](img/showcase.png)


## Logout

To logout,
1. Click "Logout" on the flyout menu (Send GET request `/logout`)
2. Redirect to the login page









