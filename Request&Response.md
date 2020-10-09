# Request & Response
# 記事の詳細機能
## Request
### Header
- userID:string
```
userID:b1018085@fun.ac.jp
```
### Body
- articleID:string
```cassandraql
{
    "articleID": "" 
}
```
 ## Response
- title : string
- imagePath : string
- context : string
- Nice : int
- NiceStatus: boolean(bool)
- ListStatus: boolean(bool)
- UserName : string
- UserImage : string
- Contents : string
```
{
    "title": "Title_sample1",
    "imagePath": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/IMG_7004.jpeg",
    "context": "五稜郭で飲んだ帰りsample1sample1sample1sample1sample1sample1sample1sample1",
    "Nice": "46",
    "NiceStatus": true,
    "ListStatus": true,
    "Comments": [
        {
            "UserName": "taketo",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "面白い"
        },
        {
            "UserName": "yamano",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "2コメ"
        },
        {
            "UserName": "sakai",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "3コメ"
        },
        {
            "UserName": "yamada",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "4コメ"
        },
        {
            "UserName": "kondo",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "5コメ"
        },
        {
            "UserName": "wakamatsu",
            "UserImage": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/sample.jp",
            "Contents": "1コメ"
        }
    ]
}
```

# 記事の一覧送信機能
## Request  
パターン1  
- genre : string
- month : string
- year  : string 

```cassandraql
{
    "genre": "" ,
    "month": "" ,
    "year": ""
}
```

 ## Response
- ArticleID : string
- Title     : string
- ImagePath : string
- Tag       : string
```cassandraql
{
    "Articles": [
        {
            "ArticleID": "1",
            "Title": "Title_sample1",
            "ImagePath": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/IMG_7004.jpeg",
            "Tag": [
                "1_sampleTag1",
                "1_sampleTag2",
                "1_sampleTag3",
                "1_sampleTag4"
            ]
        },
        {
            "ArticleID": "16",
            "Title": "Title_sample1",
            "ImagePath": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/IMG_7004.jpeg",
            "Tag": [
                "1_sampleTag1",
                "1_sampleTag2",
                "1_sampleTag3",
                "1_sampleTag4"
            ]
        },
        {
            "ArticleID": "17",
            "Title": "Title_sample1",
            "ImagePath": "https://initial-practice.s3-ap-northeast-1.amazonaws.com/IMG_7004.jpeg",
            "Tag": [
                "1_sampleTag1",
                "1_sampleTag2",
                "1_sampleTag3",
                "1_sampleTag4"
            ]
        }
    ]
}
```

# プロフィール登録
## Request
```
{
    
}
```
## Response

# ログイン画面
## Request
### Body
- mail-adress : string
- password    : string
```
{
    "mail-adress": "" ,
    "password": "" 
}
```
 ## Response
 - token : string
```
{
    "token": "aaaa" 
}
```
 # ホーム画面に遷移するたびのやりとり
## Request
- token : string
```
{
    "token": "aaaa" 
}
```
 ## Response
 ```
 {

 }
 ```
