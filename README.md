# aws_VPC_Endpoint_Guide
aws vpc endpoint 실습

## Create EC2
- BastionServer(EC2 -Public VPC) 생성
> ![스크린샷 2024-01-14 오전 12 55 28](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/6d06e2ba-87b2-47e2-a5c6-68d45f0f11ea)
> ![스크린샷 2024-01-14 오전 12 55 47](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/d39461f7-0959-4dbc-8adc-cb85fed0a935)
> ![스크린샷 2024-01-14 오전 12 56 21](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/869d4122-2fb7-4bdd-8154-be435ae9cb45)
> ![스크린샷 2024-01-14 오전 12 56 35](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/d0396ca7-2112-4566-8ce5-0498581db881)

- EndPointServer(EC2 -Private VPC) 생성
> ![스크린샷 2024-01-14 오전 12 58 10](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/bfc24cfc-f6b7-4f6c-9734-ff167794ae8a)
> ![스크린샷 2024-01-14 오전 12 58 19](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/77c72e18-3c49-4773-bc47-3756e3d9c222)
> ![스크린샷 2024-01-14 오전 12 58 40](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/6a5a9bfd-40e1-4ecf-b171-8f63c20e208f)
> ![스크린샷 2024-01-14 오전 12 58 52](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/c29af013-680c-4c88-a04c-4de2e8820786)

## Create Bucket
- S3 Bucket 생성
> ![스크린샷 2024-01-14 오전 1 01 16](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/5bedff6a-a3dc-40e2-9761-b0bd1c11e37b)

- 보안상 옳진 않지만 bucket에 키페어를 업로드 해준다. (원래는 ssh 키 포워딩을 사용해야 안전하다.)
- 보안상 키페어 업로드 이미지 생략

## BastionServer Connect
- BastionServer에 ssh로 접근한다.
- IAM에서 발급 받음 public key, private key를 입력한다.
- CLI로 S3에 연결하여 EndpointServer에 연결할 키를 다운받는다.

> ![스크린샷 2024-01-14 오전 1 15 30](https://github.com/hanmin0512/aws_VPC_Endpoint_Guide/assets/37041208/2d03b00f-7316-497b-a852-2148c395b60c)


