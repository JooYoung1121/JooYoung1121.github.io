---
title: "[리트코드] 326 Power of Three"
categories: 
  - 리트코드
last_modified_at: 2021-01-06T13:00:00+09:00
toc: true
tags: 
  - 리트코드
  - 알고리즘
published : true
---


**[Power of Three](https://leetcode.com/problems/power-of-three/)**

![문제](/assets/images/리트코드/LeetCode_326.png)


이 문제의 풀이는 굉장히 다양하게 나올 수 있습니다. 

우선 3의 승? 이라 표현해야하나 그 조건에 해당하는 숫자가 몇개 없습니다. 따라서 배열 하나에다가 해당하는 모든 숫자를 넣어서 그냥 완전탐색 돌리는 방법이 있을 수 있고, 저처럼 수학적으로 접근할 수도 있습니다. 솔루션 보면 나머지 3가지 풀이도 있으니 확인해보시면 될 것 같습니다. 

풀이는 다음과 같습니다. 

Source Code:
```cpp
class Solution {
public:
    bool isPowerOfThree(int n) {
        // x = log3n -> logn / log3 
        if(n <= 0) return false;
        double x = log10(n) / log10(3);
        
        if(fmod(x,1) == 0)
            return true;
        else 
            return false;
    }
};

```

궁금하신 점은 댓글 남겨 주세요!! 

## Summary 
- 리트코드 재밌네요