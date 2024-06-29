# YOLACT++ 인스턴스 세그멘테이션 프로젝트

## 개발 환경

### 하드웨어 스펙

- **CPU**: Ryzen 3500X
- **RAM**: 16GB
- **GPU**: GTX 1660 SUPER 6GB

### 개발 환경

- **운영체제**: Ubuntu 20.04
- **언어**: Python 3.7.16
- **주요 패키지**:
  - Torch 1.10.1+cu111
  - Torchvision 0.11.2+cu111
  - matplotlib 3.5.3
  - Numpy 1.21.5
  - Pycocotools 2.0

## 모델 세부 사항

### YOLACT++

- **Epoch**: 70
- **입력 이미지 해상도**: 1080x1080
- **Batch Size**: 1

### Total Loss 그래프

![image](https://github.com/zoid79/YOLACT/assets/87366543/0c788d63-e17b-40fa-bb12-38a8a10fa7fa)

### 성능 평가
![image](https://github.com/zoid79/YOLACT/assets/87366543/8bfd63af-0675-4cf3-9910-bf91eb7ef1b2)

논문에 따르면 이론적으로 초당 30fps 성능을 기대할 수 있지만, 현재 하드웨어 환경에서는 약 6fps로 제한되어 있습니다.


### mAP (평균 정밀도)

|     | All   | 0.5  | 0.55 | 0.6  | 0.65 | 0.7  | 0.75 | 0.8  | 0.85 | 0.9  | 0.95 |
|-----|-------|------|------|------|------|------|------|------|------|------|------|
| Box | 49.12 | 76.46| 74.58| 73.36| 68.08| 63.96| 55.51| 44.02| 26.97| 8.05 | 0.25 |
| Mask| 54.19 | 72.91| 71.51| 68.36| 66.52| 63.83| 61.89| 57.32| 43.68| 26.07| 9.79 |

| mAP by Thresholds for Box | mAP by Thresholds for Mask |
|----------------------------|----------------|
|![image](https://github.com/zoid79/YOLACT/assets/87366543/82161e2f-0318-4b13-93a4-f0d30ae3de73)|![image](https://github.com/zoid79/YOLACT/assets/87366543/e56aecff-2361-476f-a587-0b43ef4dcbd7)|


