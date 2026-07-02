```bash

# chart를 압축해서 docs 폴더 안에 저장
helm package . -d docs/
# index.yaml 파일을 docs 폴더 안에 자동 생성
helm repo index docs --url https://github.io/tkddn3901/helm-microservice/

```