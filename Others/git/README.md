# Git 사용법

## Github에 잘 못 올라간 특정 폴더 삭제하는법
만약 삭제할려는 폴더의 이름이 removedDir 라하고 삭제 방법을 적어봤다.
1. git bash를 킨다.
2. 해당 리포(repo)를 clone 한다.
3. git rm -r --cached removedDir 
4. git commit -m "해당 디렉토리를 삭제했습니다"
5. git push origin master(master나 사용중인 브랜치명)
(출처: https://youngest-programming.tistory.com/30)