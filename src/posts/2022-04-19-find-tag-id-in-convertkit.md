---
layout: post
title: How to find a tag id in Convertkit
slug: find-tag-id-in-convertkit
tags: ['convertkit']
---

Finding a tag ID in convertkit is simple. You don't need to use the API. Using the API is a roundabout way if you want to find a specific tag ID.

Here are the steps:

1. Click the tag in Convertkit
2. Look at the URL.
3. Find the `subscribable_ids` parameter

Here's an example:

```shell
https://app.convertkit.com/subscribers?subscribable_ids=3061839&subscribable_type=tag
```

In this case, the tag ID is `3061839`.
