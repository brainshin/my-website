# Terraform 에러 노트

Terraform 실습 중 자주 만나는 에러를 짧게 정리합니다.

## 예시 표

| 에러 | 원인 | 해결 방향 |
| --- | --- | --- |
| `Unsupported attribute` | 참조한 변수나 object key가 없음 | 실제 변수명과 참조명을 맞춥니다. |
| `Reference to undeclared resource` | 선언되지 않은 리소스를 참조함 | resource 이름과 참조 이름을 통일합니다. |
| `Error acquiring the state lock` | remote state lock이 남아 있음 | 실행 중인 작업 확인 후 force-unlock 여부를 판단합니다. |

## 기록 방식

에러 메시지는 원문을 남기고, 바로 아래에 원인과 실제 수정한 파일 위치를 적습니다.

[메인으로 돌아가기](../index.md)
