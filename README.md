# 도커 이미지 생성

docker build -t [이미지이름] -f [도커파일이름] .

# Docker Container 실행

docker run -d --name [컨테이너이름] -p [접속포트]:80 [이미지이름]

# 접속

localhost:[접속포트]
