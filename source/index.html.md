---
title: Mongodb Reference

search: true
---

# Video


## Get Video Actives

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "userId" : "ruby147896325@gmail.com",
                "courseId" : 728
        },
        "records" : 0.0014255167498218105,
        "update_at" : ISODate("2017-09-17T14:35:14.607Z")
}
```

影片活躍度.

### Database collection

`db.test.video_actives`

### Return Fields

Parameter | Description
--------- | -----------
records | 影片活躍度

<aside class="success">
Useful Feature.
</aside>

## Get Video Records

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("57b2015bcd5da6860db3b060"),
        "action" : "play",
        "userId" : 85831,
        "userAccount" : "B10502122@chu.edu.tw",
        "videoStartTime" : 47.497781979019166,
        "videoEndTime" : null,
        "videoId" : 30620,
        "videoTotalTime" : 2192,
        "courseId" : 919,
        "chapterId" : 5787,
        "chapterVideoCount" : 12,
        "chapterVideoOrder" : 8,
        "playRate" : 1,
        "time" : ISODate("2016-08-15T17:52:27.110Z"),
        "__v" : 0
}
```

對影片的播放、停止、搜尋動作

### Database collection

`db.test.video_records`

### Return Fields

Parameter | Description
--------- | -----------
action | play、pause、seek
playRate | play rate for video
videoTotalTime | total video time

<aside class="success">
Useful Feature.
</aside>


# Exercise

## Get Exercise Different

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "courseId" : 670,
                "exerciseId" : 3339,
                "execOrder" : 1
        },
        "update_at" : ISODate("2017-09-17T15:03:47.229Z"),
        "diff" : 0.5,
        "dift" : 1
}
```

練習題困難度

### Database collection

`db.test.exercise_diff`

### Return Fields

Parameter | Description
--------- | -----------
diff | 困難度(前27%+後27%)/2
dift | .




## Get Exercise Distance

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "courseId" : 734,
                "exerciseId" : 4029,
                "execOrder" : 3
        },
        "update_at" : ISODate("2017-09-17T15:09:50.261Z"),
        "dis" : -0.03225246091488132
}
```

練習題鑑別度.

### Database collection

`db.test.exercise_dis`

### Return Fields

Parameter | Description
--------- | -----------
execOrder | .
dis | 鑑別度 (前27%-後27%)/2



## Get Exercise Record

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("57e2e16d689eb9b30b2815e5"),
        "exerciseId" : 5655,
        "exerciseType" : "checkbox",
        "correctAns" : "1,2,5",
        "execOrder" : 1,
        "courseId" : 908,
        "getScore" : true,
        "execTotalCount" : "6",
        "userId" : 37704,
        "time" : ISODate("2016-09-21T19:37:17.285Z"),
        "studentAns" : [
                {
                        "0" : "1,2,5,"
                }
        ],
        "__v" : 0
}
```

練習題答題紀錄.

### Database collection

`db.test.exercise_records`

### Return Fields

Parameter | Description
--------- | -----------
correctAns | 正確答案
studentAns | 第幾次答題:學生的答案
getScore | 有無答對

<aside class="success">
Useful Feature.
</aside>

# Quiz

## Get Quiz Analysis

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "sid" : 1682,
                "order_num" : 1
        },
        "update_at" : ISODate("2017-03-08T17:57:38.524Z"),
        "diff" : 0.5847665847665848,
        "dift" : 0.603125,
        "dis" : 0.46683046683046686
}
```

考試鑑別度及困難度.

### Database collection

`db.test.quiz_analysis`

### Return Fields

Parameter | Description
--------- | -----------
diff | 困難度
dift | .
dis | 鑑別度

<aside class="success">
Useful Feature.
</aside>

## Get Quiz Record

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "uid" : "icourse528145",
                "sid" : 1682,
                "order_num" : 1
        },
        "getScore" : true,
        "update_at" : ISODate("2017-03-08T08:17:26.808Z")
}
```

是否有考試成績.

### Database collection

`db.test.quiz_records`



## Get Quiz Scores

> The above command returns JSON structured like this:

```json
{
        "_id" : {
                "uid" : "icourse528145",
                "sid" : 1682
        },
        "scores" : "40",
        "update_at" : ISODate("2017-03-08T08:51:04.943Z")
}
```

考試成績.

### Database collection

`db.test.quiz_scores`


# Keyword

## Get Keyword Clicks

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("5705080cf10629a45f9440a9"),
        "userId" : 1,
        "courseId" : 2,
        "chapterId" : 3,
        "videoId" : 4,
        "word" : "test str",
        "time" : ISODate("2016-04-06T12:58:52.710Z"),
        "__v" : 0
}
```

簡介.

### Database collection

`db.test.keywordclicks`

### Return Fields

Parameter | Description
--------- | -----------
word | keyword


## Get Keyword Urls

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("5885acb269e0cbd41e3280cb"),
        "userId" : 6,
        "courseId" : 848,
        "chapterId" : 5211,
        "videoId" : 25360,
        "word" : "DDoS",
        "url" : "https://www.youtube.com/embed/UTh49bqAggs?start=200&rel=0&autoplay=1",
        "text" : "反射式／放大式攻擊技術  200s",
        "time" : ISODate("2017-01-23T07:11:46.862Z"),
        "__v" : 0
}
```

簡介.

### Database collection

`db.test.keywordurls_v2`

### Return Fields

Parameter | Description
--------- | -----------
word | keyword
url | 影片連結（含時間）
text | 影片名稱+時間


# Action Records

## Get Article Actions

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("55f6aa907d5c183b5ce19a57"),
        "action" : "like",
        "userName" : "張軒銘",
        "userId" : 6272,
        "userAccount" : "a901002666@hotmail.com",
        "time" : ISODate("2015-09-14T11:08:00.643Z"),
        "object_article_info" : {
                "article_id" : 2834,
                "article_author_id" : 6,
                "article_type" : "discussion",
                "article_course_id" : 568,
                "article_chapter_id" : 2982
        },
        "__v" : 0
}
```

討論區動作紀錄（按讚、留言）.

### Database collection

`db.test.article_models`

### Return Fields

Parameter | Description
--------- | -----------
action | The action you do.(like、reply、post)
article_type | Where the action doing.

<aside class="success">
Useful Feature.
</aside>

## Get Kmap Records

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("58f724cb3ec5b68d24779353"),
        "action" : "test",
        "uid" : "test",
        "time" : "test",
        "text" : "test"
}
```

簡介.

### Database collection

`db.test.kmap_records`

### Return Fields

Parameter | Description
--------- | -----------
action | hover、click
text | .



## Get Login Records

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("57e2dc078ee8578f0be3089c"),
        "action" : "log out",
        "userId" : 6,
        "userAccount" : "nfhuang@cs.nthu.edu.tw",
        "time" : ISODate("2016-09-21T19:14:15.520Z"),
        "__v" : 0
}
```

登入、登出紀錄.

### Database collection

`db.test.login_records`

### Return Fields

Parameter | Description
--------- | -----------
action | log in、log out

<aside class="success">
Useful Feature.
</aside>

## Get Page Records

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("57b2028dcd5da6860db3b06a"),
        "action" : "leave",
        "userId" : 72511,
        "userAccount" : "aleex830625@gmail.com",
        "page" : "chapter_video",
        "description" : "1/5 video_id_is 30858",
        "courseId" : 899,
        "chapterId" : 5856,
        "time" : ISODate("2016-08-15T17:57:33.026Z"),
        "__v" : 0
}
```

每個頁面的進入、離開紀錄.

### Database collection

`db.test.page_records`

### Return Fields

Parameter | Description
--------- | -----------
action | leave、access
page | chapter_video,course_schedule,course_homepage,course_forum,chapter_exercise,course_exam

<aside class="success">
Useful Feature.
</aside>

# Other Informations

## Get Course Myth

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("58f505776e5580cb2162f434"),
        "courseId" : 987,
        "myth" : [
                {
                  "question" : 4,
                  "concept" : [
                          {
                                  "chinese" : "金融市場",
                                  "english" : ""
                          },
                          {
                                  "chinese" : "資本市場",
                                  "english" : "Capital Market"
                          },
                          {
                                  "chinese" : "股票",
                                  "english" : ""
                          },
                          {
                                  "chinese" : "股票市場交易機制",
                                  "english" : ""
                          },
                          {
                                  "chinese" : "股票信用交易",
                                  "english" : ""
                          },
                          {
                                  "chinese" : "融券放空",
                                  "english" : ""
                          }
                  ]
                }
}
```

課程迷思.

### Database collection

`db.test.article_models`

### Return Fields

Parameter | Description
--------- | -----------
myth | .
concept | .

<aside class="success">
Useful Feature.
</aside>

## Get Iitclogs

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("5824877e9953edc13def0b49"),
        "player" : "daixurl",
        "timestamp" : ISODate("2016-11-10T14:41:50.671Z"),
        "portal" : "{\"name\":\"台大醫院新竹分院鋼彈球紀念特賜\",\"plain\":\"台大醫院新竹分院鋼彈球紀念特賜 (No. 11, Lane 442, Section 1, Jingguo Road, East District, Hsinchu City, Taiwan 300)\",\"team\":\"ENLIGHTENED\",\"latE6\":24815500,\"address\":\"No. 11, Lane 442, Section 1, Jingguo Road, East District, Hsinchu City, Taiwan 300\",\"lngE6\":120980244}",
        "__v" : 0
}
```

簡介.

### Database collection

`db.test.iitclogs`

### Return Fields

Parameter | Description
--------- | -----------
player | .
portal | .




## Get Radar Informations

> The above command returns JSON structured like this:

```json
{
        "_id" : ObjectId("57f760b793392ea4cafe6b85"),
        "courseId" : 6666,
        "userId" : 6666,
        "time" : "20161007",
        "userAccount" : "wen94319@gmail.com",
        "datas" : {
                "video_finish_ratio" : 66,
                "exercise_finish_ratio" : 66,
                "actiove_ratio_person" : 66,
                "exer_ratio_person" : 66,
                "forum_ratio_person" : 66,
                "like_count" : 66
        }
}
```

雷達圖資訊.

### Database collection

`db.test.radar_informations`

### Return Fields

Parameter | Description
--------- | -----------
video_finish_ratio | 影片觀看完成率
exercise_finish_ratio | 練習題完成率
actiove_ratio_person | 影片觀看活躍度
exer_ratio_person | 練習題答對率
forum_ratio_person | 討論區參與度
like_count | 按讚次數

<aside class="success">
Useful Feature.
</aside>
