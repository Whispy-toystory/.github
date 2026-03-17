# Wispy 🧸✨
**아이의 장난감이 살아 움직이는 AI 친구**

3D 캐릭터 + 어린이 특화 LLM + 음성/AR 인터랙션을 결합한  
어린이 전용 AI 놀이 플랫폼


## Screenshots

| | | | |
|---|---|---|---|
| <img src="https://github.com/user-attachments/assets/33045467-613d-4bd6-8474-76a6f6463e03" width="220"/> | <img src="https://github.com/user-attachments/assets/c5f805ab-f9b1-4209-b34e-21c8d82eb364" width="220"/> | <img src="https://github.com/user-attachments/assets/101de016-10c6-4107-89aa-4926e2c73e36" width="220"/> | <img src="https://github.com/user-attachments/assets/298a53da-3ba8-41b1-a557-ba21f7298f4b" width="220"/> |

# Demo
👉 https://youtu.be/O17BXy2MAz8)](https://youtu.be/O17BXy2MAz8

### Vision
“아이에게 AI는 도구가 아니라 친구가 되어야 한다”

Wispy는
아이의 상상력, 감정, 사회성을 함께 키우는
AI 친구를 만들어 아이의 일상을 풍부하게 해 줍니다. 

## Overview

Wispy는 아이가 좋아하는 장난감을  
**3D 캐릭터로 변환하고, AI 친구처럼 대화**할 수 있게 해주는 서비스

- 🎨 장난감 → 3D 캐릭터 생성
- 💬 어린이 눈높이 스토리형 대화
- 🎙️ 음성 기반 인터페이스 (STT/TTS)
- 🌍 3D / AR 인터랙션

## Key Features

### Child-specialized LLM
- 짧고 쉬운 문장
- 칭찬 중심 대화
- 이야기 기반 응답 (설명 대신 상상력 유도)

### 🧸 3D Character Generation
- 이미지 → 배경 제거 → 스타일 변환 → 3D mesh 생성
- GLB 파일 생성 및 앱에서 렌더링

### 🎮 Immersive Interaction
- 3D 캐릭터 조작
- AR 환경에서 상호작용
- 터치 / 드래그 / 롱프레스 인터랙션

### 🎙️ Voice Interface
- STT (음성 입력)
- TTS (캐릭터 음성 응답)

## Architecture

```text
[iOS App]
   ↓
[Spring Boot API]
   ├── MySQL (user / metadata)
   ├── MongoDB (chat history)
   ├── S3 (3D assets)
   └── SageMaker (LLM inference)
```

## Tech Stack
### Frontend (iOS)
- Swift, UIKit, RxSwift
- SceneKit, ARKit
- Alamofire

### Backend
- Spring Boot (Java 21)
- REST API

### AI / ML
- Llama-2-7B (LoRA fine-tuning)
- 4-bit quantization (bitsandbytes)
- HuggingFace Transformers
- 3D
- rembg
- OpenCV
- Hunyuan3D

### Infra
- AWS (S3, SageMaker, EKS)
- Docker / Kubernetes
- Terraform

### Wispy LLM
- Base: Llama-2-7b-chat
- Fine-tuning: LoRA

### Dataset: 약 57만 개 (Q&A + Story 통합)
목표:
짧고 쉬운 답변
감정 중심 응답
상상력 자극

```
Repository Structure
wispy/
├── server/            # Spring Boot backend
├── ios-app/           # iOS client
├── wispy-llm/         # LLM training / inference
├── model3d/           # 3D generation pipeline
├── infra/             # Terraform / AWS
└── kubernetes/        # K8s configs

```

## Team

| Name | Role | Links |
|------|------|------|
| 송여경 | Project Lead | 🔗 [GitHub](https://github.com/0gonge) |
| 김윤희 | 3D | - |

