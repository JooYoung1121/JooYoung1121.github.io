---
title: "[리트코드] 150. Evaluate Reverse Polish Notation"
categories: 
  - 리트코드
last_modified_at: 2021-05-21T13:00:00+09:00
toc: true
tags: 
  - 리트코드
  - 알고리즘
published : true
---


**[Evaluate Reverse Polish Notation](https://leetcode.com/problems/evaluate-reverse-polish-notation/)**

![문제](/assets/images/리트코드/LeetCode_150.png)


이 문제는 전형적인 스택을 사용해서 계산기를 구현하는 것입니다. 

하지만 좀 다른점은 입력이 String으로 된다는 것입니다. 

따라서 연산자와 숫자를 어떻게 구분할지 고민하던 전 isdigit 함수를 이용한 isNumber 함수를 구현하였고 

숫자면 스택에 추가하고 연산자면 계산을 진행하는 방식으로 풀었습니다. 

풀이는 다음과 같습니다. 

Source Code:
```cpp
class Solution {
public:
    bool isNumber(string num){
        for(auto n : num){
            if(n == '-' && num.length() == 1) return false;
            if(n == '-') continue;
            if(!isdigit(n))
                return false;
        }
        return true;
    }
    
    int evalRPN(vector<string>& tokens) {
        stack<int> st;
        for(auto token : tokens){
            if(isNumber(token)){
                st.push(stoi(token));
            }else{
                int a = st.top();
                st.pop();
                int b = st.top();
                st.pop();
                if(token == "+") st.push(b+a);
                if(token == "-") st.push(b-a);
                if(token == "*") st.push(b*a);
                if(token == "/") st.push(b/a);
            }
        }
        return st.top();
    }
};

```

궁금하신 점은 댓글 남겨 주세요!! 

## Summary 
- 많은 피드백 부탁드리겠습니다. 