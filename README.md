# Quote Porn

## Overview

Quote Porn is a prototype of a simple quote engine. It provides REST APIs for light-weight integration with other services.
It has been created to satisfy your hard-core desire for daily motivation. If your mind craves for a quick get-away to hear
witty statements from the celebrities, then `quoteporn` is the way to go.

## How It Works  
![alt text](https://raw.githubusercontent.com/jayeshathila/quoteporn/master/quoteporn.jpg)

### Feed Quotes:
- 1. Add quotes to `quotes` file
- 2. Raise PR.
- 3. Get it merged and voila, done.
### Consume Quotes:
- Just hit - [quoteporn](https://quoteporn.fun) .

## REST APIs 

- Getting Motivational Quotes:
  
  HTTP Method: GET 
  
  Endpoint: `https://quoteporn.fun/`
  
  Sample Usage:
    ```python
    import requests
    
    url = "https://quoteporn.fun/"
    
    headers = {
        'User-Agent': "PostmanRuntime/7.15.0",
        'Accept': "*/*",
        'Cache-Control': "no-cache",
        'Postman-Token': "042f2fd1-c725-4494-97a1-5d4d72d8cf55,57bad808-b1e6-44cc-abb8-d2c28d9deeaf",
        'Host': "quoteporn.fun",
        'accept-encoding': "gzip, deflate",
        'Connection': "keep-alive",
        'cache-control': "no-cache"
        }
    
    response = requests.request("GET", url, headers=headers)
    
    print(response.text)
    ```
    
- Getting Celebrity Quotes:
  HTTP Method: GET 
  
  Endpoint: `https://quoteporn.fun/`
  
  Sample Usage:
    ```python
    import requests
    
    url = "https://quoteporn.fun/tv_series"
    
    headers = {
        'User-Agent': "PostmanRuntime/7.15.0",
        'Accept': "*/*",
        'Cache-Control': "no-cache",
        'Postman-Token': "3050d723-05f2-4427-89b6-fb95e91f4768,4e8acd8a-3627-47a1-b680-83ae3efe3bc8",
        'Host': "quoteporn.fun",
        'accept-encoding': "gzip, deflate",
        'Connection': "keep-alive",
        'cache-control': "no-cache"
        }
    
    response = requests.request("GET", url, headers=headers)
    
    print(response.text)
    ```

## LPT (Life Pro Tip)

- Bookmark  
As usual, one of the advantage of GET requests is that they can be bookmarked for quick access.

- Shell Alias  
If you are a CLI fan, you can save it as a shell alias.
```bash  
$ cat ~/.bashrc
alias motivate="
curl -X GET \
  https://quoteporn.fun/tv_series \
  -H 'Accept: */*' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Host: quoteporn.fun' \
  -H 'Postman-Token: 3050d723-05f2-4427-89b6-fb95e91f4768,0c561954-0e60-40c4-a431-3d0e30a1af4f' \
  -H 'User-Agent: PostmanRuntime/7.15.0' \
  -H 'accept-encoding: gzip, deflate' \
  -H 'cache-control: no-cache';
echo"
$ . ~/.bashrc
$ motivate
"Caring makes you weak. If they think you care, they'll walk all over you. - Suits"
```   

- Recurring Schedule  
You can set a recurring schedule for your quote message by integrating with unix [watch](https://en.wikipedia.org/wiki/Watch_(Unix) utility.

## Message from the Creator 

[Creator](https://github.com/jayeshathila) of the Quote Porn says - 

Use it when:
- You are stuck on something, and need a little push.
- Your coffee ain't caffeinated enough for your dark-theme terminal.
- You want to start your day with a plain old motivational quote.

## Stats
![visitors](https://visitor-badge.glitch.me/badge?page_id=jayeshathila.quoteporn)	![code-size](https://img.shields.io/github/languages/code-size/jayeshathila/quoteporn)