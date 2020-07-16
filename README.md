# React widget API

使用 Next.js 的 API Routes 建立的 API，用於 [react-widget](https://github.com/Airwavess/react-widget) 專案。

## API

API HOST 為 https://react-widget-api.vercel.app/。

僅提供 GET 取得資料，如果使用其他 HTTP 方法則會回傳 405。

**圖片資源**

`GET /api/v1/images`

```
curl -i https://react-widget-api.vercel.app/api/v1/images
HTTP/1.1 200 OK
[
  {
    "id":"image1",
    "url":"https://source.unsplash.com/-87JyMb9ZfU/400",
    "title":"Jerry Zhang image",
    "content":"Jerry Zhang"
  }
]
```

`GET /api/v1/images/[id]`

```
curl -i https://react-widget-api.vercel.app/api/v1/images/image1
HTTP/1.1 200 OK
{
  id: "image1",
  url: "https://source.unsplash.com/-87JyMb9ZfU/400",
  title: "Jerry Zhang image",
  content: "Jerry Zhang"
}
```

**影片資源**

`GET /api/v1/videos`

```
curl -i https://react-widget-api.vercel.app/api/v1/videos
HTTP/1.1 200 OK
[
  {
    id: "video1",
    url: "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerFun.mp4",
    title: "For Bigger Fun video",
    content: "Jerry Zhang"
  }
]
```

`GET /api/v1/videos/[id]`

```
curl -i https://react-widget-api.vercel.app/api/v1/videos/video1
HTTP/1.1 200 OK
{
  id: "video1",
  url: "http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerFun.mp4",
  title: "For Bigger Fun video",
  content: "Jerry Zhang"
}
```
