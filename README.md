# Recommendation system & Item embedding

### Theory
#### 1. Content based filtering => 비슷한 User를 Mapping하여 추천한다. 코사인 유사도 사용.
#### 2. nearest neighbor based filtering => 비슷한 User를 Mapping하여 평가점수를 예측하여 추천한다. 
#### 3. User based filtering => 비슷한 User와 Item을 Mapping 하여 평가점수를 예측하여 유사한 User에게 아이템을 추천한다.
#### !but, 아이템이 많은 경우 비슷한 Item과 User를 Mapping하기에 너무 Sparse하다. 
#### 4. Latent factor based filtering => 2개의 matrix(User - Item, fature-Item)를 통하여 User - Item 의 행렬을 계산하여 추천한다.  

### Story Line
#### 추천!!
#### 1. e-커머스에서 N개의 제품을 판매하는 중. 
#### 2. 특정 User에게 유사한 Item을 추천, 같이 판매되는 보조Item을 추천
#### 3. 비슷한 User를 Clustering하여 가장 좋은 Item을 추천

#### 재고예측!!
#### 1. 특정Item을 기반으로 User를 군집한다. (ex. 단백질 보충제 => 다이어트를 하는 고객, 운동을 하는 고객 등) 
#### 2. 주요factor를 분리한다. (ex. 계절성, 재구매성으로 Rating)
#### 3. 상위Rank의 제품을 추천하거나 재고를 보관한다. 


### Technical detail
#### 추천!!
#### 1. e-커머스에서 N개의 제품을 판매하는 중. ==> NoSQL ex.{purchase: list, Pur_date: list, view: list} 
#### 2. 특정 User에게 유사한 Item을 추천, 같이 판매되는 보조Item을 추천 ==> Content based filtering
#### 3. 비슷한 User를 Clustering하여 가장 좋은 Item을 추천 ==> Word2Vec, GloVe과 같은 Embedding, 유사한 Vector를 추출  

#### 재고예측!!
#### 1. 특정Item을 기반으로 User를 군집한다. ==> Word2Vec, GloVe과 같은 Embedding, 유사한 Vector를 추출
#### 2. 주요factor를 분리한다. 
#### 3. 상위Rank의 제품을 추천하거나 재고를 보관한다. 
