---
title: "[리트코드] 104 Maximum Depth of Binary Tree"
categories: 
  - 리트코드
last_modified_at: 2021-01-01T13:00:00+09:00
toc: true
tags: 
  - 리트코드
  - 알고리즘
published : true
---


**[Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)**

![문제](/assets/images/리트코드/LeetCode_104.png)


전 이런 종류의 문제는 너무 어려워하는게 큰 문제인거같습니다. 

이런 종류를 많이 풀면서 공부를 해야 겠습니다. 

recursive로 풀이를 하였고 한단계 내려갈때마다 +를 해주되 왼쪽과 오른쪽 노드중에서 가장 큰 깊이로 반환하는 방식으로 풀이했습니다. 

풀이는 다음과 같습니다. 

Source Code:
```cpp
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    int maxDepth(TreeNode* root) {
        if(!root) return 0;
        
        return 1 + max(maxDepth(root->left),maxDepth(root->right));
    }
};

```

궁금하신 점은 댓글 남겨 주세요!! 

## Summary 
- 이런 종류 문제는 전 어려워요 ㅠㅠ