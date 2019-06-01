## QQMusicAPI

!> QQ音乐API koa2 版本, 通过Web网页版请求QQ音乐接口数据, 有问题请提 [issue](https://github.com/Rain120/qq-music-api/issues), 或者你有其他想法欢迎`PR`.

## API结构图

![qq-music](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/qq-music.png)

## API接口

!> koa接口说明(参数, 地址, 效果图)

### 获取QQ音乐产品的下载地址

接口说明: 调用此接口, 可获取QQ音乐标准产品下载链接

接口地址: `/downloadQQMusic`

示例截图:

![获取QQ音乐产品的下载地址](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/downloadQQMusic.png)

### 获取热词

接口说明: 调用此接口, 可获取搜索热词

接口地址: `/getHotkey`

示例截图:

![获取搜索热词](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/gethotkey.png)

### 获取歌单分类

接口说明: 调用此接口, 可获取歌单分类, 包含`category`信息

接口地址: `/getSongListCategories`

<details>
  <summary>SortID</summary>

    sortId: 1, sortName: 默认
    sortId: 2, sortName: 最新
    sortId: 3, sortName: 最热
    sortId: 4, sortName: 评分
    sortId: 5, sortName: none
</details>

**歌单分类(categoryId & categoryName)**

<details>
  <summary>1. 热门</summary>

    1.1
      "categoryId": 10000000,
      "categoryName": 全部,
</details>

<details>
  <summary>2. 语种</summary>
  
    2.1
      "categoryId": 167,
      "categoryName": "英语",
    2.2
      "categoryId": 168,
      "categoryName": "韩语",
    2.3
      "categoryId": 166,
      "categoryName": "粤语",
    2.4
      "categoryId": 169,
      "categoryName": "日语",
    2.5
      "categoryId": 170,
      "categoryName": "小语种",
    2.6
      "categoryId": 203,
      "categoryName": "闽南语",
    2.7
      "categoryId": 204,
      "categoryName": "法语",
    2.8
      "categoryId": 205,
      "categoryName": "拉丁语",
</details>

<details>
  <summary>3. 流派</summary>

    3.1
      "categoryId": 6,
      "categoryName": "流行",
    3.2
      "categoryId": 15,
      "categoryName": "轻音乐",
    3.3
      "categoryId": 11,
      "categoryName": "摇滚",
    3.4
      "categoryId": 28,
      "categoryName": "民谣",
    3.5
      "categoryId": 8,
      "categoryName": "R&B",
    3.6
      "categoryId": 153,
      "categoryName": "嘻哈",
    3.7
      "categoryId": 24,
      "categoryName": "电子",
    3.8
      "categoryId": 27,
      "categoryName": "古典",
    3.9
      "categoryId": 18,
      "categoryName": "乡村",
    3.10
      "categoryId": 22,
      "categoryName": "蓝调",
    3.11
      "categoryId": 21,
      "categoryName": "爵士",
    3.12
      "categoryId": 164,
      "categoryName": "新世纪",
    3.13
      "categoryId": 25,
      "categoryName": "拉丁",
    3.14
      "categoryId": 218,
      "categoryName": "后摇",
    3.15
      "categoryId": 219,
      "categoryName": "中国传统",
    3.16
      "categoryId": 220,
      "categoryName": "世界音乐",
</details>

<details>
  <summary>4. 主题</summary>

    4.1
      "categoryId": 39,
      "categoryName": "ACG",
    4.2
      "categoryId": 136,
      "categoryName": "经典",
    4.3
      "categoryId": 146,
      "categoryName": "网络歌曲",
    4.4
      "categoryId": 133,
      "categoryName": "影视",
    4.5
      "categoryId": 141,
      "categoryName": "KTV热歌",
    4.6
      "categoryId": 131,
      "categoryName": "儿歌",
    4.7
      "categoryId": 145,
      "categoryName": "中国风",
    4.8
      "categoryId": 194,
      "categoryName": "古风",
    4.9
      "categoryId": 148,
      "categoryName": "情歌",
    4.10
      "categoryId": 196,
      "categoryName": "城市",
    4.11
      "categoryId": 197,
      "categoryName": "现场音乐",
    4.12
      "categoryId": 199,
      "categoryName": "背景音乐",
    4.13
      "categoryId": 200,
      "categoryName": "佛教音乐",
    4.14
      "categoryId": 201,
      "categoryName": "UP主",
    4.15
      "categoryId": 202,
      "categoryName": "乐器",
    4.16
      "categoryId": 14,
      "categoryName": "DJ",
</details>

<details>
  <summary>5. 心情</summary>

    5.1
      "categoryId": 52,
      "categoryName": "伤感",
    5.2
      "categoryId": 122,
      "categoryName": "安静",
    5.3
      "categoryId": 117,
      "categoryName": "快乐",
    5.4
      "categoryId": 116,
      "categoryName": "治愈",
    5.5
      "categoryId": 125,
      "categoryName": "励志",
    5.6
      "categoryId": 59,
      "categoryName": "甜蜜",
    5.7
      "categoryId": 55,
      "categoryName": "寂寞",
    5.8
      "categoryId": 126,
      "categoryName": "宣泄",
    5.9
      "categoryId": 68,
      "categoryName": "思念",
</details>

<details>
  <summary>6. 场景</summary>

    6.1
      "categoryId": 78,
      "categoryName": "睡前",
    6.2
      "categoryId": 102,
      "categoryName": "夜店",
    6.3
      "categoryId": 101,
      "categoryName": "学习",
    6.4
      "categoryId": 99,
      "categoryName": "运动",
    6.5
      "categoryId": 99,
      "categoryName": "运动",
    6.6
      "categoryId": 76,
      "categoryName": "约会",
    6.7
      "categoryId": 94,
      "categoryName": "工作",
    6.8
      "categoryId": 81,
      "categoryName": "旅行",
    6.9
      "categoryId": 103,
      "categoryName": "派对",
    6.10
      "categoryId": 222,
      "categoryName": "婚礼",
    6.11
      "categoryId": 223,
      "categoryName": "咖啡馆",
    6.12
      "categoryId": 224,
      "categoryName": "跳舞",
    6.13
      "categoryId": 16,
      "categoryName": "校园",
  </summary>
</details>

示例截图:

![获取歌单分类](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSongListCategories.png)

### 获取歌单列表

接口说明: 调用此接口, 可获取歌单列表

参数列表:

- 必选参数

`categoryId`: 类别`id`

- 可选参数

`page`: 当前页数, 默认为1

`limit`: 取出歌单数量, 默认为 20

`sortId`: 最新, 最热,评分,  默认为5

接口地址: `/getSongLists`

调用例子: `/getSongLists?categoryId=10000000`

示例截图:

**获取歌单列表**

![获取歌单列表](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSongLists.png)

**获取歌单列表-带参数**

![获取歌单列表-带参数](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSongLists-params.png)

### 获取歌单详情

接口说明: 调用此接口, 可获取歌单详情

参数列表:

- 必选参数

`disstid`: 歌单`id`

接口地址: `/getSongListDetail`

调用例子: `/getSongListDetail?disstid=7011264340`

示例截图:

![获取歌单详情](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSongListDetail.png)

### 获取MV标签

接口说明: 调用此接口, 可获取MV标签

接口地址: `/getMvByTag`

调用例子: `/getMvByTag`

示例截图:

![获取MV标签](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getMvByTag.png)

### 获取歌手MV

接口说明: 调用此接口, 可获取歌手MV

参数列表:

- 必选参数

`singermid`: 歌手`id`

- 可选参数

`order`: 当前MV类型, 默认为`time`

- `listen`: 歌手专辑音乐MV

- `time`: 粉丝上传MV视频

`limit`: 取出歌单数量, 默认为5

接口地址: `/getSingerMV`

调用例子: `/getSingerMV?singermid=0025NhlN2yWrP4&order=all&limit=5`

示例截图:

![获取歌手MV - default](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSingerMv-default.png)

![获取歌手MV - belong](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSingerMv-listen.png)

![获取歌手MV - fans](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSingerMv-time.png)

### 获取相似歌手

参数列表:

- 必选参数

`singermid`: 歌手`id`

接口说明: 调用此接口, 可获取相似歌手

接口地址: `/getSimilarSinger`

调用例子: `/getSimilarSinger?singermid=0025NhlN2yWrP4`

示例截图:

![获取相似歌手](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSimilarSinger.png)

### 获取歌手信息

参数列表:

- 必选参数

`singermid`: 歌手`id`

接口说明: 调用此接口, 可获取歌手信息

接口地址: `/getSingerDesc`

调用例子: `/getSingerDesc?singermid=0025NhlN2yWrP4`

示例截图:

![获取歌手信息](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getSingerDesc.png)

### 获取电台列表

参数列表:

接口说明: 调用此接口, 可获取电台列表, 分类

接口地址: `/getRadioLists`

调用例子: `/getRadioLists`

示例截图:

![获取电台列表](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getRadioLists.png)

### 获取专辑

参数列表:

- 必选参数

`albummid`: 专辑`id`

接口说明: 调用此接口, 可获取专辑信息(专辑列表、详情)

接口地址: `/getAlbum`

调用例子: `/getAlbum?albummid=0016l2F430zMux`

示例截图:

![获取专辑](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getAlbum.png)

### 获取数字专辑

参数列表:

接口说明: 调用此接口, 可获取数字专辑, 轮播图`banner`, 专辑列表等信息, 详见[API结构图](#API结构图)

接口地址: `/getDigitalAlbumLists`

调用例子: `/getDigitalAlbumLists`

示例截图:

![获取数字专辑](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getDigitalAlbumLists.png)

### 获取歌曲歌词

- 必选参数

`songmid`: 专辑`id`

- 可选参数

`isFormat`: 是否格式化歌词, 默认值为 `false`

参数列表:

接口说明: 调用此接口, 可获取歌曲歌词

接口地址: `/getLyric`

调用例子: `/getLyric?songmid=003rJSwm3TechU`

示例截图:

![获取歌曲歌词 - 未格式化](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getLyric.png)

![获取歌曲歌词 - 格式化](https://raw.githubusercontent.com/Rain120/qq-music-api/master/screenshot/getLyric-parse.png)