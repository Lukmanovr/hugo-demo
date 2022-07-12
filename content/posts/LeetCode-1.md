---
title: "Running python terminal with Pyscript"
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
description: "Running interactive python repl"
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

<p></p>
As an exercise we will use the leetcode solution of the 2Sum problem (using 2-pointer approach).
Problem description: Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target. You may assume that each input would have exactly one solution, and you may not use the same element twice.

```
    def twoSum(nums, target):
        nums_index = [(v, index) for index, v in enumerate(nums)]
        nums_index.sort()
        begin, end = 0, len(nums) - 1
        while begin < end:
            curr = nums_index[begin][0] + nums_index[end][0]
            if curr == target:
                return [nums_index[begin][1], nums_index[end][1]]
            elif curr < target:
                begin += 1
            else:
                end -= 1

    nums = [4,2,5,2,3,7,4, 8]
    target = 6
    twoSum(nums, target)
```

Now, let's try to run this code here in the browser using Pyscript and repl. Just copy, paste the code into interactive Python repl and press the green button.

<h3>Interactive Python Repl</h3>
<div>
    <script defer src="https://pyscript.net/alpha/pyscript.js"></script>
        <h4><a href="/posts/leetcode-1/">Clear All</a></h4>
    <py-repl id="repl" auto-generate="True"></py-repl>
</div>
