# Multi-Modal U-Net (mmUnet)

이 프로젝트는 PyTorch를 사용하여 여러 가지 변형된 UNet 모델을 구현한 것입니다. **사용한 데이터셋은 이전 프로젝트와 동일합니다.** 데이터 전처리, 모델 정의, 학습 스크립트 및 모델 저장/로드 유틸리티가 포함되어 있습니다.

## 목차
- [요구 사항](#요구-사항)
- [프로젝트 구조](#프로젝트-구조)
- [사용법](#사용법)
  - [데이터 전처리](#데이터-전처리)
  - [모델 학습](#모델-학습)
  - [모델 테스트](#모델-테스트)
  - [GIF 생성](#gif-생성)
- [모델 아키텍처](#모델-아키텍처)
- [감사의 말](#감사의-말)

## 요구 사항
- Python 3.x
- torch
- numpy
- matplotlib
- Pillow

필요한 패키지 설치:
```sh
pip install -r requirements.txt

프로젝트 구조
.
├── 0_train.py             # 학습 스크립트
├── 1_test.py              # 테스트 스크립트
├── backbone.py            # 모델의 백본 네트워크
├── create_gif.py          # TIF 이미지를 GIF로 변환하는 스크립트
├── data_loader.py         # 데이터 로드 및 증강 스크립트
├── data_preprocess.py     # 데이터 전처리 스크립트
├── multi_unet2d.py        # Multi-modal UNet 모델 정의
├── multi_unet2d_attention.py  # Attention 기반 Multi-modal UNet 모델 정의
├── multi_unet2d_r2.py     # R2 기반 Multi-modal UNet 모델 정의
├── multi_unet2d_r2att.py  # R2Attention 기반 Multi-modal UNet 모델 정의
├── unet_model.py          # 기본 UNet 모델 정의
├── utils.py               # 유틸리티 함수
└── README.md              # 프로젝트 문서
