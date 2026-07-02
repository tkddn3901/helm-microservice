```bash

# chart를 압축해서 docs 폴더 안에 저장
helm package . -d docs/
# index.yaml 파일을 docs 폴더 안에 자동 생성
helm repo index docs --url https://tkddn3901.github.io/helm-microservice/
# git push 후 github pages

# 현재 등록된 helm 저장소 목록 조회
helm repo ls
# 방금 만든 helm chart의 위치를 helm 저장소로 등록
helm repo add msa https://tkddn3901.github.io/helm-microservice/
# 저장소에 있는 내용을 모두 받아올 수 있도록 동기화
helm repo update
# 저장소에 어떤 chart가 들어있는지 검색
helm search repo msa
# install 해보기
helm install msa-release msa/msa-platform -n msa --create-namespace

```