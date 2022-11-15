# Docker Image 생성 ()

docker build -t [이미지이름] -f [도커파일이름] .

# Docker Container 실행

docker run -d --name [컨테이너이름] -p [접속포트]:80 [이미지이름]

# 접속

localhost:[접속포트]





---------------------------------------------

# AWS EC2에 React, NginX 배포하기

local

0. Docker hub 이동 레포지토리 생성
1. Docker Image 생성 ( docker build -t [이미지이름] -f [도커파일이름] . )
2. Docker Container 실행 ( docker run -d --name [컨테이너이름] -p [접속포트]:80 [레포지토리사용자이름]/[레포지토리명] )
3. Docker Container를 통한 이미지 생성 (docker commit [컨테이너이름] [레포지토리사용자이름]/[레포지토리명])
4. Docker hub 이미지 올리기 ( Docker push [레포지토리사용자이름]/[레포지토리명] )

ec2
1. EC2 생성 (docker 설치, 패키지 업데이트, ssh 접속)
2. EC2 인바운드 그룹 편집
3. sudo docker run --name [컨테이너이름] -p [접속포트]:80 -dt [레포지토리사용자이름]/[레포지토리명]

