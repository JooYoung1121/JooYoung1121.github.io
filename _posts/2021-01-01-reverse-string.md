---
title: "[리트코드] 344 Reverse String"
categories: 
  - 리트코드
last_modified_at: 2021-01-01T13:00:00+09:00
toc: true
tags: 
  - 리트코드
  - 알고리즘
  - 구현
published : true
---

새해 첫날입니다!! 오늘부터 매일 매일 하나씩 리트코드 문제를 풀어보려고 합니다.

리트코드는 영어로 되있다는 단점이 있지만 문제를 어떻게 풀어야 효율적으로 풀 수 있는지를 여러 사람들과 토론하며 고민하며 풀 수 있다는 장점이 있습니다. 

저에겐 큰 도움이 될거같아서 시작하게 되었습니다. 

**[Reverse String](https://leetcode.com/problems/reverse-string/)**

![문제](/assets/images/리트코드/LeetCode_344.png)

보면 진짜 간단한 문제입니다. 배열을 역으로 만들어주면 되지만 단순하게 접근한다면 이중포문을 사용해서 시간복잡도가 n^2가 될수도 있고 불필요한 배열을 하나 더 생성하여 공간복잡도가 증가할 수 있습니다. 

하지만 투포인터를 사용하여 처음과 끝 숫자를 변경해주면서 진행한다면 시간복잡도가 n으로 줄어들 수 있습니다. 

풀이는 다음과 같습니다. 


Source Code:
```cpp
class Solution {
public:
    void reverseString(vector<char>& s) {
        int Start = 0, End = s.size()-1;
        while(Start < End){
            char tmp = s[Start];
            s[Start++] = s[End];
            s[End--] = tmp;
        }
    }
};

```

궁금하신 점은 댓글 남겨 주세요!! 

## Summary 
- 새해 복 많이 받으세요!! 
- 2021년엔 제가 부지런하길 기원하고 있습니다. 