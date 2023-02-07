# Sysinfocus SpotAssist 1.0
This is a tiny utility to perform routine tasks and create code repository for internal use. This utility has the ability to store any text as template and recall it based on the shortcut name given. It can also be used to process templated data.

# It's FREE!

## Upcoming features
- Ability to query MSSQL Server database.
- Ability to query SQLite database.

## Version Update
- 1.0.2 (7-Feb-2023)
  - Type `~>open help` and copy to land on this page.
  - More templates to process - `{Day}`, `{Month}`, `{Year}`, `{Weekday}`, `{Up}`, `{UTCDate}`, `{UTCTime}`, `{UTCDateTime}`
  - More convesions - `~>process-tobase64`, `~>process-frombase64`, `~>process-repeat`

- 1.0.1 (5-Feb-2023)
  - Now shows errors, if any on the console.

## Videos
[![Open any website from anywhere using Sysinfocus SpotAssist 1.0](https://img.youtube.com/vi/0Y5MYQE9KlI/0.jpg)](https://www.youtube.com/watch?v=0Y5MYQE9KlI)
[![Power of Sysinfocus SpotAssist 1.0](https://img.youtube.com/vi/8NaXb9HgN6g/0.jpg)](https://www.youtube.com/watch?v=8NaXb9HgN6g)


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
~>process-comma
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

9. You have some text that needs to be converted to Base64?

```
~>process-tobase64
Your Text Here
```
When you copy the text starting with ~>process and paste anywhere, you will get the following output.
```
WW91ciBUZXh0IEhlcmUNCg==
```

10. You have some Base64 encoded that needs to be converted to plain text?

```
~>process-frombase64
WW91ciBUZXh0IEhlcmUNCg==
```
When you copy the text starting with ~>process and paste anywhere, you will get the following output.
```
Your Text Here
```

11. You want something to repeat or generated serial numbers for a given range?

```
~>process-repeat
1-100
<~
Line No. {i}
```
When you copy the text starting with ~>process and paste anywhere, you will get the following output.
```
Line No. 1
Line No. 2
Line No. 3
Line No. 4
Line No. 5
Line No. 6
Line No. 7
Line No. 8
Line No. 9
Line No. 10
Line No. 11
Line No. 12
Line No. 13
Line No. 14
Line No. 15
Line No. 16
Line No. 17
Line No. 18
Line No. 19
Line No. 20
Line No. 21
Line No. 22
Line No. 23
Line No. 24
Line No. 25
Line No. 26
Line No. 27
Line No. 28
Line No. 29
Line No. 30
Line No. 31
Line No. 32
Line No. 33
Line No. 34
Line No. 35
Line No. 36
Line No. 37
Line No. 38
Line No. 39
Line No. 40
Line No. 41
Line No. 42
Line No. 43
Line No. 44
Line No. 45
Line No. 46
Line No. 47
Line No. 48
Line No. 49
Line No. 50
Line No. 51
Line No. 52
Line No. 53
Line No. 54
Line No. 55
Line No. 56
Line No. 57
Line No. 58
Line No. 59
Line No. 60
Line No. 61
Line No. 62
Line No. 63
Line No. 64
Line No. 65
Line No. 66
Line No. 67
Line No. 68
Line No. 69
Line No. 70
Line No. 71
Line No. 72
Line No. 73
Line No. 74
Line No. 75
Line No. 76
Line No. 77
Line No. 78
Line No. 79
Line No. 80
Line No. 81
Line No. 82
Line No. 83
Line No. 84
Line No. 85
Line No. 86
Line No. 87
Line No. 88
Line No. 89
Line No. 90
Line No. 91
Line No. 92
Line No. 93
Line No. 94
Line No. 95
Line No. 96
Line No. 97
Line No. 98
Line No. 99
Line No. 100
```
