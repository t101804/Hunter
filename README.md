
<head>
<div class="header" align="center">
    <a href="https://repcyber.com"><img src="static/icon.png" alt="Hunter"></a>
    <h1>Hunter by @repproject</h1>
  </div>
</head>

<h4 align="center">This repository contains a Hunter. applications that can be used for parsing or scrapping multiple server / hosts for getting big web-data using custom resources and reproject api's.</h4>


<p align="center">
<a href="https://github.com/t101804/Hunter/releases"><img src="https://img.shields.io/github/downloads/t101804/Hunter/total">
<a href="https://github.com/t101804/Hunter/graphs/contributors"><img src="https://img.shields.io/github/contributors-anon/t101804/Hunter">
<a href="https://github.com/t101804/Hunter/releases/"><img src="https://img.shields.io/github/release/t101804/Hunter">
<a href="https://github.com/t101804/Hunter/issues"><img src="https://img.shields.io/github/issues-raw/t101804/Hunter">
<a href="https://github.com/t101804/Hunter/discussions"><img src="https://img.shields.io/github/discussions/t101804/Hunter">
<a href="https://t.me//repproject"><img src="https://img.shields.io/discord/695645237418131507.svg?logo=telegram"></a>
</p>
      
<p align="center">
  <a href="https://github.com/t101804/Hunter/blob/main/README_VIP.md">Buy VIP API Access RepProject</a> •
  <a href="#why-not-open-source-?">Why not open source?</a> •
  <a href="#install-hunter">Install</a> •
  <a href="#documentation">Documentation</a> •
  <a href="#credits">Credits</a> •
  <a href="https://t.me//repproject">Join Telegram</a>
</p>

## The art of speed , lightweight and highly customizable

Feel free to contact me to buy access for accesing all repproject api's : 
- [Telegram](https://t.me//CallMeRep)
- [Youtube](https://youtube.com/@CallMeRep)

## Why not open source ?

Back to explaining what Hunter is. Hunter is used to send requests across targets based on a config, leading to zero false positives and providing fast parsing,scanning and scrapping on a large number of lists and pages. Hunter using multiple method parameter to use in templates config. With powerful and flexible config templates, Hunter can be used to model all kinds of web scrapping and i think in the future no one helping me with this project so i decided to not opensources :) . [Click here](#documentation) to know more about use customing config templates

# Install Hunter

Hunter not requires anything because its already compiled . it works on cross-platforms such as Unix,Windows and MacOS

Unix/Linux System

```sh
git clone https://github.com/t101804/Hunter.git 
cd Hunter 
chmod +x hunter_linux 
./hunter_linux 
```
If you using get error "/lib/x86_64-linux-gnu/libc.so.6: version not found do command : 
```sh
sudo add-apt-repository 'deb http://cz.archive.ubuntu.com/ubuntu jammy main'
sudo update
sudo apt install libc6
```
<details>
  <summary>Windows</summary>
  <a href="https://github.com/t101804/Hunter/archive/refs/heads/main.zip">Download directly</a>
</details>
<details>
  <summary>MacOS</summary>
  <p> Same as Unix/linux system but run ./hunter_macos </p>
</details>

# Documentation
here are 3 documentations : 
- [application](#application)
- [server repproject](#server-repproject-vip)
- [custom server](#custom-server)


## Application
Basic config documentation is for the applications in config.json
```json
"application": {
        "apikey_repproject": "your_apikey_that_you_got_from_buy_access",
        "reqtimeout": 60,   
        "reqmaxbytes": "50mb",
    },
```
1. the <b>"apikey_repproject"</b> is apikey server that will send to repcyber api's if your ip is registered in system you will can be accessed the server. to buy apikey and authorize your ip you can buy from me in [here](https://t.me//callmerep) starts with 20$ only 

2. the <b>"reqtimeout"</b> is a each requests timeout so if the response server is more then 60 seconds it will skip 

3. the <b>"reqmaxbytes"</b> is a each requests max results response, so if each results is more then 50mb it wil only grab the 50mb and the rest is auto skip

## Server RepProject VIP
Basic config documentation for repproject server 
```json
"server": {
        "server_reverse_ip": {
          "all records ( grab all of records )": "https://repcyber.com/allreverse/{ip}",
          "a records ( a tld domains only )": "https://repcyber.com/reverse/{ip}",
          "ns records ( nameserver only )": "https://repcyber.com/revip_ns/{ip}",
          "mx recods ( mailserver only )": "https://repcyber.com/revip_mx/{ip}",
          "cname records ( cname only )": "https://repcyber.com/revip_cname/{ip}"
        },
        "server_grabber": {
          "grab ip records": "https://repcyber.com/vipgrab/ip/{total}",
          "grab amazon records": "https://repcyber.com/vipgrab/amazonaws.com/total/{total}",
          "grab tld domain records": "https://repcyber.com/vipgrab/tld_domains/{total}"
        },
        "server_utility": {
          "analyze site ( check cms and tech )": "https://repcyber.com/analyzer/{site}",
          "cpanel checker": "https://repcyber.com/checker/cpanel/{raw_lists}"
        }
    },
```
<b> for this you can check https://t.me//repproject and you can only using this if you alredy buy and get the apikey </b>
<p> before using please check server is alive or no and always check channel for more info </p>

## Custom Server

```json
    "custom_server": {
        "urcustomname": {
            "custom_header": [],
            "method": "",
            "post_data": "",
            "regex": "",
            "url": ""
        },
        "examples_custom_config_for_reverse_rapid_methods_GET": {
            "custom_header": [
                "Content-Type:*/*",
                "User-agent:Mozilla/5.0"
            ],
            "method": "get",
            "post_data": "",
            "regex": "<td>(.*?)</td>",
            "url": "https://rapiddns.io/sameip/{ip}?full=1"
        },
        "examples_custom_config_for_reverse_seoaudit_methods_POST": {
            "custom_header": [
                "referer:tools.seo-auditor.com.ru/check-ip/"
            ],
            "method": "post",
            "post_data": "url={ip}",
            "regex": "<th align=\"left\" nowrap>\u0414\u043E\u043C\u0435\u043D:<\/th>\\s+<td width=\"100%\">(.*?)<\/td>",
            "url": "https://tools.seo-auditor.com.ru/tools/check-ip/"
        }
        
    }
```
<b>make sure u put "," if you want add a new custom name again if you have any json error make sure you make a valid json type </b>

<b>you can add unlimited custom server you want</b>

### "url"  ( must fill )
you can put the url and if url have parameter you can put the parameter

## "{parameter} ( must fill )
you can fill whatever you want and this have 3 parameter that you can use in URL or POST_DATA 
- {page} : loop the page examples you put 50 page it will loop 1-50 with threadings 
- {total} : the total pages its using manual loopings ( if you confuse please watch the vidio ) 
- {site} : make sure the lists have format sitelist type then run the parameter 
- {ip} : if the lists is site is auto change to ip then run the parameter 
- {raw_lists} : run the lists without filtering anything
### "method" ( must fill )
this only have 2 method "get" and "post" only ( make sure its lowercase )

### "custom_header" ( additional, you can keep blank )
example usage : 
- ```"custom_header": ["Content-Type:*/*", "User-agent:Mozilla/5.0"],```


### "post_data ( use this if you using post method )" 
example usage :
- ```"post_data": "param1=value&param2=value2",```
- you can also use parameter ```"post_data": "ip={ip}",```
### "regex" ( keep it blank if you want save all pages ): 
<b>if your regex contains " escape with \ so it will be \" for the escape</b>
example usage :
- ```"regex": "/site/(.*?)\""```

# Credits : 
https://t.me//CallMeRep
<!-- ## Custom-server templates instuctions
```json
"": {
    "url": "",
    "method": "",
    "custom_header": [""],
    "post_data": "",
    "regex": ""
},
```
1. "url" :

2. "method" :

3. "custom_header" :

4. "post_data" : 

5. "regex" :  -->
