# How to Favicon in 2021

**Author:** Blog  
**Full title:** How to Favicon in 2021  
**URL:** https://www.bram.us/2020/12/26/how-to-favicon-in-2021/  
**Source:** #articles #instapaper #readwise

- Having only this in your markup will do nowadays:
  <link rel="icon" href="/favicon.ico"><!-- 32×32 -->
  <link rel="icon" href="/icon.svg" type="image/svg+xml" sizes="any">
  <link rel="apple-touch-icon" href="/apple.png"><!-- 180×180 -->
  <link rel="manifest" href="/manifest.webmanifest"> 
   
- Along with this in your linked manifest.webmanifest
  {
  "icons": [
  { "src": "/192.png", "type": "image/png", "sizes": "192x192" },
  { "src": "/512.png", "type": "image/png", "sizes": "512x512" }
  ]
  } 
   
