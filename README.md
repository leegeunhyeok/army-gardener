<div align="center">

# army-gardener

👨‍🏭 군 훈련소 기간동안 잔디밭을 책임져줄 든든한 정원사

</div>

## Feature

> 🌱 매일 오전 9시에 잔디를 심어드립니다. (UTC 00:00)

## Setup

1. 상단의 `Use this template` 버튼 눌러 Fork
2. [.github/workflows/planting-grass.yml](.github/workflows/planting-grass.yml) 파일 수정
   - 파일 내에 표기해둔 `A`, `B` 작업 진행
3. 수정사항 커밋 후 푸쉬!
   - `(주의)` 커밋 시 사용자 정보(이름 및 이메일)가 깃허브 계정과 일치해야 잔디가 심어집니다.

### Disable

- `(비활성)` 이전에 진행했던 A, B 작업 이전으로 되돌리면 더 이상 자동으로 커밋하지 않습니다!

## How it works?

[GitHub Actions](https://github.com/features/actions)의 스케줄링(crontab) 기능을 통해 매일 본 저장소의 `task.sh` 스크립트를 실행합니다.  
스크립트는 현재 날짜(`yyyy-MM-dd`)값을 받아 `date.txt` 파일에 기록하며,  
해당 변경 사항을 커밋하고 원격 저장소로 푸쉬함으로써 그 날의 잔디를 심습니다.  

깃 사용자 정보(이름 및 이메일)는 이전 커밋 기록을 기준으로 자동 추출하며,  
결과적으론 [Setup](#setup) 과정에서 커밋을 수행한 사용자 정보를 사용하게 됩니다.

> 스크립트가 실행되면서 날짜 값이 `date.txt` 파일에 한 줄씩 누적됩니다!

## Meter

본인은 산업기능요원으로 재직 중이며, 훈련소 기간동안 커밋을 못할 생각을 하니 ~~잘 심어두었던 잔디가 걱정되었다~~.  
이러한 이유로 빠르고 대충 만들게된 쉽고 간편하고 편리한 GitHub Actions 템플릿 저장소!

~~그대로 방치하면 군 문제가 아니더라도 평생 자동으로 잔디를 심을 수 있다.~~

## Issue

- 오전 9시에 액션이 실행되도록 구성되어있지만, 깃허브 서버 상태에 따라 약간의 지연이 발생할 수 있음
