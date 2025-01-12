# 베이스 이미지 설정
FROM node:lts-alpine

# 작업 디렉터리 설정
WORKDIR /app

# package.json, package-lock.json 복사
COPY package*.json ./

# 의존성 설치
RUN npm install

# 소스 코드 복사
COPY . .

# 빌드
RUN npm run build

# 빌드된 파일을 Nginx 컨테이너로 복사하기 위해 export
CMD ["npm", "run", "serve"]