# 🏆 2024 소프트웨어중심대학 공동 딥러닝 챌린지

## 📌 개요
🎯 **Zero-shot Classification을 위한 딥러닝 모델 평가**

- **대회 일정:** 2024년 7월 26일 ~ 8월 30일 오후 5시 (KST)
- **평가 기준:** Kaggle Final Score (Private Score 기준, 동점자의 경우 제출 시간으로 순위 재산정)
- **목표:** Vision Language Model (VLM) 기반의 **Zero-shot Classification** 성능 평가

---

## 🔍 대회 설명
이 대회에서는 **VLM(Vision Language Model)** 을 활용하여 한 번도 학습하지 않은 **테스트 이미지 데이터**의 레이블을 예측해야 합니다. **Zero-shot Learning**의 대표적인 예시로 **CLIP**이 있으며, 본 대회에서는 제공된 테스트 데이터셋을 **학습할 수 없습니다.**

- **데이터 구성:**
  - 총 **8,100개 이미지**
  - **6개 클래스**
  - 이미지 크기: **(224, 224, 3)**
- **제약 사항:**
  - 제공된 데이터셋을 **학습 과정에 포함하는 것은 금지**됨 (supervised, unsupervised, self-supervised 학습 모두 포함)
  - **사전 학습된 모델을 활용**할 수 있으며, **Prompt Tuning, Adapter 등을 이용한 성능 향상 가능**
  - 학습된 모델을 활용해 테스트 데이터의 label을 예측한 후, **CSV 파일로 Kaggle에 제출**

---

## ⚙️ 사용한 모델
본 프로젝트에서는 **여러 Hugging Face의 Zero-shot 모델**을 사용하여 성능을 비교하고 조합하였습니다.

### ✅ **사용한 VLM 모델**
1️⃣ **OpenCLIP** - 오픈소스로 공개된 CLIP 모델

2️⃣ **EvaCLIP** - CLIP을 개선한 고성능 모델

3️⃣ **JinaCLIP** - JinaAI에서 공개한 CLIP 변형 모델

4️⃣ **SLGLIP** - 더 강력한 이미지-텍스트 매핑 기능을 가진 모델

5️⃣ **DFN (DFN5B)** - 가장 높은 성능을 보인 모델

### ✅ **성능 비교**
- **단일 모델 성능**: DFN5B 모델이 가장 높은 정확도를 기록
- **Ensemble 기법**: **5개 모델을 Weight Voting 방식으로 결합하여 최상의 성능을 도출**

---

## 📊 모델 성능 평가
- 단일 모델 중 **DFN5B가 가장 우수한 성능**을 보임
- 5개의 모델을 **Weighted Voting Ensemble**하여 최적의 성능을 달성


## 🚀 경험 및 결론
- **입상에는 실패했지만**, Hugging Face의 다양한 Zero-shot 모델을 실험해볼 수 있는 좋은 경험이었음.
- 여러 **VLM 모델을 비교하고 앙상블 기법을 활용**하여 성능을 개선하는 방법을 익힘.
- **Zero-shot Learning과 Vision-Language Model의 실전 활용 경험**을 쌓을 수 있었음.

📌 **향후 개선 방향:**
- 더 많은 사전 학습 모델 실험 (e.g., BLIP, Flamingo 등)
- **Prompt Engineering 및 Fine-tuning 기법 활용**을 통한 추가 성능 향상
- **Ensemble 기법 개선** (Stacking, Bagging 등 다양한 방법 테스트)

---

## 📚 참고 자료
- **Hugging Face 모델:** [Hugging Face Model Hub](https://huggingface.co/models)
- **Kaggle 대회 페이지:** [kaggle](https://www.kaggle.com/c/2024swunivchallenge/overview)

---

## 📝 라이선스
📌 **MIT License**

