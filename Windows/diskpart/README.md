# distpart

- RPi 등에 사용하는 SD 카드는 파티션이 많이 분리되어 있어서, 윈도우에서 사용 시 드라이브 인식 과정에서 문제가 발생할 수 있음
- 파티션을 모두 없애고 단일 파티션으로 만드는 방법
  - diskpart 실행
  - list disk 명령으로 SD 카드 확인
  - select disk X 명령으로 SD 카드 선택 (여기서 X는 SD 카드의 번호)
  - clean 명령 입력하면 모든 파티션 지워지고 하나만 남음
- 다음으로 SD Card Formatter 등의 도구를 사용해서 포멧
  