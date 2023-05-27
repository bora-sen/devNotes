## There is a way to translate strings.
You need to send a **GET Request** to following url;
```http
GET http://https://translate.googleapis.com/translate_a/single?client=gtx&sl=<SourceLanguage(tr,en,etc.)>&tl=<TargetLanguage(tr,en,etc.)>&dt=t&q=<URLEncodedString(Hello%20World)>
```

This **Get Request** should return something like this.

```json
[[["Merhaba","Hello",null,null,10]],null,"en",null,null,null,null,[]
```


```js
// You can refer translated text
const req = await fetch(URL)
const resp = await req.json()
const translatedText = resp[0][0][0]
```
