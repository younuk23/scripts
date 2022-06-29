## Remote Repository branch 삭제 (master, main, develop 제외)
`git branch -r | egrep -v "(^\*|master|main|develop)" | sed s/origin///g | xargs -I {} echo git push origin :{}`

## 특정 디렉토리 필터링 후 삭제
`sudo du -h --max-depth=1 /var/lib/jenkins/workspace/ | grep M | awk '{print $2}' | xargs -I {} sudo rm -rf {}`



