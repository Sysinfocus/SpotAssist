# Sysinfocus SpotAssist 1.0
This is a tiny utility to perform routine tasks and create code repository for internal use. This utility has the ability to store any text as template and recall it based on the shortcut name given. It can also be used to process templated data.

# It's FREE!

## Upcoming features
- Ability to query MSSQL Server database.
- Ability to query SQLite database.

## Version Update
- 1.0.1 (5-Feb-2023)
  - Now shows errors, if any on the console.

## How to use?
- Download `SpotAssist.zip` file and extract it to any folder.
- Run `SpotAssist.exe` the only file in the .zip, which is a console application.
- When this app is running, you can do all the following things mentioned in the examples below.

**Note**: This is the first release of this application. If you come across any issues, just open *'Issues'* here in **GitHub**, will try to resolve. This application currently runs only on Windows 10/11 operating systems.


## Examples
1. To open a website, type and copy `~>open http://google.com` and boom! your website is opened.

2. To open a folder in your PC, type and copy `~>open c:\foldername` and boom! your folder is opened if exists, else will open the Documents folder by default.

3. To create template
```
+>shortcut_name
Line 1
Line 2
Line 3
```
Copy the lines starting with +> to create template

4. To recall template data
```
=>shortcut_name
```
Copy the lines starting with => and when you paste, you will get the templated data.

5. To process templated data
```
~>process
This will be the template. You can have {Guid}, {Date}, {Time} or {DateTime} automatically injected.
You can also have placeholders like {$1} and {$2} which will be replaced by comma separated data provided below the process terminator.
<~
Data1,Data2
Data3,Data4
Data5,Data6
```
Copy the lines starting with ~> and when you paste, you will have something like this
```
This will be the template. You can have f3b5914a-1efd-4bfa-a874-7b980690a156, 01-02-2023, 14:58 PM or 01-02-2023 14:58:28 automatically injected.
You can also have placeholders like Data1 and Data2 which will be replaced by comma separated data provided below the process terminator.
This will be the template. You can have d262943b-87ab-45ce-b9d7-bb5d5ce5286e, 01-02-2023, 14:58 PM or 01-02-2023 14:58:28 automatically injected.
You can also have placeholders like Data3 and Data4 which will be replaced by comma separated data provided below the process terminator.
This will be the template. You can have ad807a7a-cfed-4410-9ad5-7956457a007b, 01-02-2023, 14:58 PM or 01-02-2023 14:58:28 automatically injected.
You can also have placeholders like Data5 and Data6 which will be replaced by comma separated data provided below the process terminator.
```

6. To query an API right within your text-editor:
```
~>process-api
GET https://api.github.com/users/github
User-Agent: Notepad
<~
```
Copy the lines starting with ~>process-api and when you paste it anywhere, you will see the below response available for you.
```
Status Code: OK
Response Time: 6ms

{
  "login": "github",
  "id": 9919,
  "node_id": "MDEyOk9yZ2FuaXphdGlvbjk5MTk=",
  "avatar_url": "https://avatars.githubusercontent.com/u/9919?v=4",
  "gravatar_id": "",
  "url": "https://api.github.com/users/github",
  "html_url": "https://github.com/github",
  "followers_url": "https://api.github.com/users/github/followers",
  "following_url": "https://api.github.com/users/github/following{/other_user}",
  "gists_url": "https://api.github.com/users/github/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/github/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/github/subscriptions",
  "organizations_url": "https://api.github.com/users/github/orgs",
  "repos_url": "https://api.github.com/users/github/repos",
  "events_url": "https://api.github.com/users/github/events{/privacy}",
  "received_events_url": "https://api.github.com/users/github/received_events",
  "type": "Organization",
  "site_admin": false,
  "name": "GitHub",
  "company": null,
  "blog": "https://github.com/about",
  "location": "San Francisco, CA",
  "email": null,
  "hireable": null,
  "bio": "How people build software.",
  "twitter_username": null,
  "public_repos": 452,
  "public_gists": 0,
  "followers": 16595,
  "following": 0,
  "created_at": "2008-05-11T04:37:31Z",
  "updated_at": "2022-11-29T19:44:55Z"
}
```

7. You have some text separated with Tabs and want it to be converted to Comma separated?

```
~>process-tocomma
1	2	3	4	5	6	7	8	9	10
<~
```
When you copy the text starting with ~>process and paste anywhere, you will get the following output.
```
1,2,3,4,5,6,7,8,9,10
```

8. You have some text separated with Comma and want it to be converted to Tab separated?

```
~>process-totab
1,2,3,4,5,6,7,8,9,10
<~
```
When you copy the text starting with ~>process and paste anywhere, you will get the following output.
```
1	2	3	4	5	6	7	8	9	10
```
