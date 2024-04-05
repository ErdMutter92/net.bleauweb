---
title: "Angular Dynamic I18N"
date: 2024-04-04T23:13:31-04:00
draft: true
---

When working on the "Learning with Wikipedia" project I found that I wanted to make it so that it supported multiple languages. When implementing this feature I then realized that I might also want to make it so that the UI is in the targeted language. After reading back up on angular's built in i18n solution I realized that I did not want to deploy multiple versions of the web application to github pages, and instead needed a dynamic means of translating the website. That is what I am here to talk about today. How does one create a system within Angular for dynmaically swapping out translation files? Continue reading to find out.

<!--more-->

```TypeScript
import { Pipe } from "@angular/core";

@Pipe({
    name: "translate"
})
export class Translate {}
```