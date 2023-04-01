# tidyverse를 이용한 data handling

## 강의1
* 임상데이터를 분석하려면, 본인이 분석하고자 하는대로 데이터를 자유롭게 핸들링해야함 ->가장 최적화된 패키지: tidyverse
* tidyverse: dplyr, ggplot2, forcats, tibble, stringr, readr, tidyr, purrr 라는 패키지들의 집합체 패키지임
* tidyverse의 근간을 이루는 주요 명령어: select, filter, arrange, mutate, summerize, group_by 등

## 강의2 
* select 기능:특정 variable을 select 하는 함수
* select 함수를 사용하여 특정 열만 추출하거나, 특정 열을 제외시키거나, 변수명 변경이 가능하고, |> 파이프를 사용하여 readable하고 직관적으로 코드를 정리할 수 있음.

## 강의3
* filter 기능
:특정 조건을 만족하는 행을 끌고 오는 함수로 select와 같이 사용하여 조건문(AND, OR) 만들 수 있음. 복합조건문을 쓸 때는 괄호 사용하여 원하는 조건을 묶어줘야 함. 
* count -> 분포(수량)를 확인하는 함수로 이 기능은 data exploration에 매우 유용
* is.na와 !is.na 기능을 사용하여 결측값이 있는지 확인하거나 결측값을 제외하고 필터링 가능

## 강의4
* mutate 기능
:기존 데이터에 없던 새로운 변수를 만들어내는 기능으로, 임상연구 데이터에서는 주로 조건에 따라 grouping을 하는 경우가 많음. 
* 조건을 이용하여 새로운 변수 만들기: ifelse()함수 사용. 
* 변수 값의 순서를 설정할 경우:min_rank() <-오름차순으로 rank, 그 역은 min_rank(desc())
* 연속형 변수-> 범주형 변수로 변경: cut함수 사용

## 강의5
* Arrange: 오름차순, 내림차순으로 정렬하는 기능
* summarise: 개별 데이터를 뭉쳐서 특정한 값을 보여주는 것. Summarise 기능이 유용한 이유는 group_by 함수를 함께 사용하여
그룹별 값을 구할 수 있기 때문. 
 -> Summarise 할 때, 결측치가 있는 값일 경우 na.rm =T 해줘야함. 
  ( na.rm에서 rm은 remove. 즉, na값은 제거해라 ) 
* Distinct: 중복값을 제외하고 고유의 값만 추출하는 함수



