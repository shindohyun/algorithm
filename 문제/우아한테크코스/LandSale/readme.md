## 토지분양

#### 문제 설명

물 좋고 공기 좋은 강원도 양양의 한 개발자 마을 토지를 분양받고자 합니다.
토지는 직사각형 형태로 분양받을 수 있으며, x축(수평 방향)과 y축(수직 방향)에 의해 만들어지는 2차원 평면에서
두 점 P1(x1, y1)과 P2(x2, y2)로 표현할 수 있습니다. 마을 곳곳에는 식수원이 존재하여,
이미 분양된 토지와 겹치지 않으며 식수원 일부를 포함한 토지를 분양받고자 합니다.

![img](https://camo.githubusercontent.com/6eda858006fe4132f4a1dddbec08cba165fc245f/68747470733a2f2f67726570702d70726f6772616d6d6572732e73332e616d617a6f6e6177732e636f6d2f66696c65732f70726f64756374696f6e2f653461306263666135332f32636263613664362d346634362d343338392d616133652d6430653230376461353635322e706e67)

위의 예에서 이미 분양된 토지와 겹치지 않으며 식수원을 포함하고 있으므로 분양 가능합니다.

이미 분양된 토지별 위치를 담은 이차원 배열 lands와 식수원별 위치를 담은 이차원 배열 wells,
분양받고자 하는 토지의 위치를 담은 배열 point가 매개변수로 주어질 때,
토지분양이 가능한지 판별하여 return 하도록 solution 메서드를 완성해주세요.

#### 제한사항

- lands와 wells의 길이는 1 이상 10,000 이하입니다.
- lands와 wells의 원소(토지와 식수원의 위치)는 [x1, y1, x2, y2]로 들어있습니다.
- point의 길이는 4입니다.
- point에는 점이 [x1, y1, x2, y2]로 들어있습니다.
- x 좌표와 y 좌표는 0 이상 1,000,000 이하인 정수입니다.

#### 입출력 예

| lands                                                 | wells                                  | point            | result |
| ----------------------------------------------------- | -------------------------------------- | ---------------- | ------ |
| [ [10, 0, 30, 5], [0, 30, 20, 50], [30, 30, 40, 40] ] | [ [15, 15, 25, 25], [40, 10, 50, 20] ] | [10, 10, 30, 30] | true   |
| [ [0, 0, 20, 10], [10, 20, 20, 40], [30, 0, 50, 20] ] | [ [20, 40, 30, 50], [30, 20, 50, 30] ] | [20, 30, 30, 40] | false  |

#### 입출력 예 설명

입출력 예 #1
문제의 예시와 같습니다.

입출력 예 #2
이미 분양된 토지와 겹치지 않지만 식수원 일부를 포함하고 있지 않아 분양받을 수 없습니다.