# No-as-a-Service
In a world of `Things-as-a-Service`, there is a very simple thing which is missing! It's a very basic one, but it's one of the most difficult things in our every day lives. Here it's implemented and provided FREE OF CHARGE!

Sometimes the only possible answer you can give is `NO`. It's not easy, but saying NO is good:

- it's `BETTER` than not responding at all (which may very often be a way to hide a NO, trying to delay the consequences)
  - >I've finished the toilet paper, can you help me? ...

- it's `WAY BETTER` than saying YES and not following through
  - >Can you help me finding my way back home? YES (and going away instantly)
  - >Will I have your support for this thing? YES (and then disappearing in key moments)

- it `INSTANTLY` tells the other party that the question itself contains one or more defects or unmet expectations
  - >(every minute while driving) Are we there yet? NO
  - >Since you're blonde, I think you're a very cute brunette! NO!

- it `MAY` open up a feedback request for improvement
  - >Am I ready for the next step? No! Why? Well, it's because...

- it `MAY` be followed by a clarification sentence, like `NO, but...`, `No, because..`
  - >Doctor I'm sick and I thought this pill can help me! NO, but you can take this one instead!

- it `PREVENTS` wars or very bad things to happen
  - >Should we use a nuclear weapon? NO!
  - >Is it safe to use the toilet without checking for paper first? NO
  - >(after hours of hair styling) Can I touch your hair? NO!

>You already know VERY WELL what are the NO side-effects and consequences, so we can just skip them!

>Btw, this SOFTWARE is PROVIDED AS-IS. WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, and Bla Bla Bla...you won't read till here anyways, so why bothering writing it?

If you're reading this, I've sold you the service :tada:! So let's get to the details!

## Getting started
Easiest way to express a NO is a Boolean `false` value. Saying NO is already difficult, so let's keep it simple stupid! (Wow KISS Principle applied!)

Many different ways to say no:

### cURL
`curl https://gotev.github.io/no-as-a-service/request.json`

### JavaScript
```javascript
fetch('https://gotev.github.io/no-as-a-service/request.json')
  .then(responsePayload => responsePayload.json())
  .then(responseJson => console.log(responseJson))
```

### OkHttp (Java Virtual Machine & Android) - written in Kotlin
```kotlin
val client = OkHttpClient()
val request = Request.Builder()
    .url("https://gotev.github.io/no-as-a-service/request.json")
    .build()

client.newCall(request).enqueue(object : Callback {
    override fun onFailure(call: Call, e: IOException) {
        // Do something with your error
    }

    override fun onResponse(call: Call, response: Response) {
        // do something with the response
    }
})
```

### iOS
```swift
let session = URLSession.shared
let requestUrl = URL(string: "https://gotev.github.io/no-as-a-service/request.json")!

session.dataTask(with: requestUrl, completionHandler: { data, response, error in
    if let error = error {
        print(error)
        return
    }
    
    guard let data = data else { return }
    
    // Do something with the response
}).resume()
```

## Contributing
Contributing is easy, just open a PR with your idea! It can be providing a new code example, improving an existing one, extending this README. Let's make `NO` great again!

## License
Getting formal here. Prepare your best suit & tie before reading!

Ehm..suit & tie first, thanks!

```
Copyright 2020 Aleksandar Gotev

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
