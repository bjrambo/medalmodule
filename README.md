## 경험치 모듈

기존의 경험치 모듈에서 메달 기능을 추가한 모듈입니다.

## 라이선스

기존의 라이선스를 그대로 이어 GPL V2 이며 누구든지 이 코드를 수정하여 사용 배포 할 수 있습니다.

## 사용시 주의사항

### 1.1.0 버전 이후
앞으로는 XE의 모든 호환성은 깨지게 됩니다.
XE에서 사용하기 위해서는 1.0.0 버전을 이용하시길 바랍니다.
1.1.0버전에서 더 이상 lang.xml 파일은 쓰지 않습니다.

lang/lang.xml 파일은 FTP상에서 반드시 삭제 하고 ko.php 파일을 업로드될 수 있도록 해주세요.

### 2021년 5월 12일 업데이트 이후

업데이트 이후 모든 포인트 변동사항이 월별 활동으로 책정될 수 있습니다.
관리자페이지에서 회원의 경험치를 수정하는 경우는 월 활동량에 반영되지 않습니다.
그리고 월 활동에 반영되지 않도록 포인트를 변경 하고 싶으시면 항상 코드작성시 `experienceController::getInstance()->setExperience($member_srl, intval(5), 'add', false)` 와 같이 마지막 인자를 false 으로 전달하시기 바랍니다.

### 2020년 12월 18일 이후 커밋된 코드를 사용하길 권장합니다.

그 이전의 코드를 사용하다 문제발생시 저희는 책임지지 않습니다.
12월 초 배포버전을 사용하는 사람은 다음달 1월이 되기전까지 무조건 업데이트를 하여야 정상적으로 작동을 보장받습니다. 업데이트 하지 않아 생기는 과실은 본 저작권자가 책임지지 않습니다. (미리 경고 및 안내를 드립니다.)
https://xetown.com/updatenews/1492641 관련 글

## 1.0.0
* 월별 경험치 활동 기록을 트리거뿐만 아니라 모든 기록에 포함시키도록함
	* 단 관리자 페이지에서 수정하는 변경사항은 월별 활동 수치에 기록되지 않음

## 0.1.1
* 경험치 증가에도 불구하고 매달의 경험치가 지급되지 않는 문제 고침.
* 마지막 브론즈메달 지급의 갯수가 설정값과 다르게 적용되는 문제 고침.
