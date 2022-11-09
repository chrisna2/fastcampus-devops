# Docker for windows : sh 파일 사용방법

## step 1 : sh 파이를 ps1 파일로 변경 한다

- sh파일을 powershell 프로그램으로 기동하는 것은 힘들다
- poweshell 스크립트느 .ps1 파일을 통해 기동 가능 
- .bat 파일도 기동이 가능하다
- sh 파일 안에 전체 적인 문법이 docker 콘솔로만 일루어 진 경우 쉽게 가능하다
- 만약 bash , env 와 같은 linux shell 스크립트 문법이 섞인 경우 ps1의 문법에 맞춰 주어야 한다.

## step 2 : 서명이 되지 않은 ps1도 실행 가능하도록 설정한다.

```console
$ Set-ExecutionPolicy Unrestricted

실행 규칙 변경
실행 정책은 신뢰하지 않는 스크립트로부터 사용자를 보호합니다. 실행 정책을 변경하면
about_Execution_Policies 도움말 항목(https://go.microsoft.com/fwlink/?LinkID=135170)에 설명된 보안 위험에
 노출될 수 있습니다. 실행 정책을 변경하시겠습니까?
[Y] 예(Y)  [A] 모두 예(A)  [N] 아니요(N)  [L] 모두 아니요(L)  [S] 일시 중단(S)  [?] 도움말
(기본값은 "N"):Y

```

## step 3 : ps1 파일이 있는 경로에 접근하여 .ps1 파일을 실행 한다.