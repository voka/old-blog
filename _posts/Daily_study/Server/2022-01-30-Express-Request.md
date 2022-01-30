---
title: "Express-Request"
categories:
  - Web
toc: true
toc_sticky: true
tags:
  - Study
  - Android
  - web
  - Javascript
  - Server
  - REST API
  - Express
---

### Express 사용시 req.params와 req.body 차이점

## @ req.params

> url로 들어오는 요청을 가져옵니다.

예시로 아래와 같은 코드가 있을 경우

```javascript
router.get("/test/:id", auth, async (req, res) => {
  // 'id'라는 프로퍼티

  try {
    const { id } = req.params;
    console.log(id);
  } catch (err) {
    res.status(500).send("Server Error");
  }
});
```

> GET 서버아이피/test/byebye로 요청을 보냈을 경우 req.params는 byebye가 됩니다.

## @ req.body

> 'request body'에 'key-value'의 데이터가 담긴 객체 프로퍼티이다. JSON 객체에 접근 가능

예시로 아래와 같은 코드가 있을 경우

```javascript
app.post("/test", (req, res) => {
  console.log(req.body.test);
});
```

Post로 다음과 같은 요청을 보낼 경우

```json
{
  "test": "byebye"
}
```

req.body.test는 byebye가 됩니다.
