---
title: "Leetcode 2Sum problem"
date: 2022-06-03T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Leetcode", "Python", "Problem"]
author: "Rustam A. Lukmanov"
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "First try of the leetcode problems"
canonicalURL: "https://canonical.url/to/page"
disableHLJS: false # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
cover:
    image:  # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "mailto:mail@rustam-lukmanov.ru"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Solution of the 2Sum problem on leetcode using 2-pointer approach.
Problem description: Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice.

```
    class Solution:
    def twoSum(self, nums, target):
        # two point
        nums_index = [(v, index) for index, v in enumerate(nums)]
        #print(nums_index)
        nums_index.sort()
        #print(nums_index)
        begin, end = 0, len(nums) - 1
        while begin < end:
            curr = nums_index[begin][0] + nums_index[end][0]
            if curr == target:
                return [nums_index[begin][1], nums_index[end][1]]
            elif curr < target:
                begin += 1
            else:
                end -= 1
```

Now, let's try to run this code here in the browser using Pyscript and repl:

<div>
    <script defer src="https://pyscript.net/alpha/pyscript.js"></script>
        <h4><a href="/posts/leetcode-1/">Clear All</a></h4>
    <py-repl id="repl" auto-generate="True"></py-repl>
</div>
