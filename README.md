# D-market-Server-V1

## 개발 진행 방식
1. `issue` 생성 (라벨 및 assigness 설정)
2. `issue`를 기반으로 브랜치 생성
3. 브랜치를 Head로 하여, 라벨에 맞게 구현
4. 커밋 규칙에 맞춘 PR 및 Merge Commit 생성
* Merge 허용 원칙
  * conflict가 없어야합니다.
  * 서버 개발자 수 / 2 (최대 4명) 명의 코드리뷰를 받아야합니다.
  * SonarCloud를 적용할 경우, CodeSmell이 없어야합니다.
5. Squash and Merge를 진행합니다.
6. issue를 close합니다.


## commit 규칙
> :이모티콘: :: (#이슈번호) 줄거리

:bulb: 만일 이슈번호가 없는 경우, 생략이 가능합니다.

| 이모티콘 종류 | 의미 | 
|---|:---:|
| :sparkles:(`sparkles`) | 기능 추가 |
| :hammer:(`hammer`) | 기능 수정 |
| :triangular_flag_on_post:(`triangular_flag_on_post`) | 기능 삭제 |
| :recycle:(`recycle`) | 리펙토링 |
| :ambulance:(`ambulance`) | 핫픽스 |
| :bookmark:(`bookmark`) | 버전 업데이트 |
| :rocket:(`rocket`) | Pull Request |
| :bug:(`bug`) | 버그 수정 |
| :white_check_mark:(`white_check_mark`) | 테스트케이스 작성 |
| :lock:(`lock`) | 보안 추가 및 변경 |
| :wrench:(`wrench`) | 설정 추가 및 변경 |
| :construction_worker:(`construction_worker`) | CI 추가 |
| :heavy_plus_sign:(`heavy_plus_sign`) | dependency 추가 |
| :heavy_minus_sign:(`heavy_minus_sign`) | dependency 삭제 |
| :memo:(`memo`) | document 추가 및 수정 |

예시)
issue 3782, README.md 수정 -> :memo: :: (#3782) README.md 수정


## issue 규칙
> issue template를 반드시 사용하여 규격에 맞게 작성한다.
> 기능 한 개의 issue를 생성한 후, 진행합니다.


## label 규칙
> issue 및 PR에서 손쉽게 확인하기 위해 추가해야합니다.
> 라벨은 각 하나씩만을 사용해야합니다. (test 라벨 제외)

| 라벨명 | 라벨 의미 |
|---|:---:|
| bug | 버그가 발생하였을 경우, 확인하기 위한 라벨 (오직 이슈에서만 사용할 것) |
| refactor | 리펙토링을 진행해야하는 경우, 사용하는 라벨 |
| hotfix | 핫픽스를 진행해야하는 경우, 사용하는 라벨 |
| setting | 프로젝트에 설정이 필요한 경우, 사용하는 라벨 (초기 세팅 혹은 CI 등) |
| feat | 기능을 추가하거나 수정하는 경우, 사용하는 라벨 | 
| test | 기능 구현에 대해 테스트를 수정해야하는 경우, 추가하는 라벨 (단독으로 사용하여서는 안됩니다.) |


## merge 규칙
> merge는 반드시 PR 커밋 이모티콘(:rocket:)을 사용하여 커밋을 하며, github에서만 진행합니다. <br>
> 커밋 메시지 뒤에 붙는 PR 이슈 번호는 반드시 삭제한 후 진행합니다. <br>
> 예) :rocket: :: (#36282) 냉장고 냉기 차단 기능 추가 (#36283) -> :rocket: :: (#36282) 냉장고 냉기 차단 기능 추가 <br>
> Squash and Merge만을 통해서 main 브랜치에 병합합니다. <br>


## PR 규칙
> PR는 반드시 github을 통해서만 진행합니다.


## branch 규칙
> <Feature/Hotfix/Refactor/Setting>/#이슈번호 이슈제목 <br>
> 예) Feature/#25 IPhone 결제 서비스 추상화

