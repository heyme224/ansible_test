## 실습을 위해 gabia 에서 domain 을 하나 구매한다
### 아래와 같은 순서대로 실행한다
```bash
ansible-playbook ec2_bootstrap.yml

# nginx 설치
ansible-playbook nginx_setup.yml

# certbot 를 이용해서 인증서 발급
ansible-playbook certbot_setup.yml

# https 환경에서 nginx 가 동작하도록 설정
ansible-playbook nginx_https.yml

# fastapi WAS 실행
ansible-playbook fastapi_setup.yml