---
title: "임베딩"
date: 2020-07-14
categories: NLP
---

1. 전이학습
신경망의 일부 도는 젗네 신경망 가중치 파라미터를 MLE를 통해 학습데이터에 본격적으로 훈련시키기에 앞서, 다른 데이터셋이나 목적함수를 사용해 미리 훈련한 후, 이를 바탕으로 본격적으로 학습에서 신경망 가중치 파라미터를 더 쉽게 최적화하게 하는 것

사전 훈련된 단어 임베딩 벡터를 사용하지 않는 이유
- 문장의 문맥을 반영하지 못하는 기존 단어 임베딩 알고리즘 
    word2vec, Skip-gram, GloVe 알고리즘은 문장에 함께 출현한 단어들을 예측하는 데 기반. 임베딩된 정보 매우 한정적. 
    해당 알고리즘들의 목적함수는 우리가 실제 수행하려는 문제를 해결하기 위한 목적 함수와 매우 다를 것
    
    
 word2vec
 1) CBOW (Continuous Bag Of Word): 주변에 나타나는 단어들을 원핫 인코딩된 벡터로 입력받아 해당 단어를 예측
 2) Skip-gram : 대상 단어를 원핫 인코딩된 벡터로 입력받아 주변에 나타나는 단어를 예측. 
 
 GloVe(gloval vectors for word representation): 대상 단어에 대해서 코퍼스에 함께 나타난 단어별 출현 빈도를 예측, 분류문제가 아닌 출현 빈도를 근사하는 회귀 문제. 
 
 
 출처: 김기현의 자연어 처리 딥러닝 캠프 파이토치편
