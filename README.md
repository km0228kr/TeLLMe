# TeLLMe: Therapeutic Embrace LLM Evolve



<p align="center">
  <tr>
    <td><img src="https://github.com/user-attachments/assets/c861bbd0-e72a-4494-a71d-9156e7d1685c" width="400"></td>
    <td><img src="https://github.com/user-attachments/assets/2fec2504-feea-40ef-914d-d14ed56cc8f3" width="425"></td>
  </tr>
</p>

# CBT 상담 모델 강화 프로젝트

## 프로젝트 개요
- **프로젝트 기간**: 2024년 3월 ~ 2024년 11월
- **프로젝트 주제**: CBT(인지행동치료) 기반의 상담 모델 강화
- **백본 모델**: Camel

### 백본 모델 설명
Camel은 연세대학교 인공지능학과와 심리학과 공동 연구팀이 개발한 심리상담 특화 인공지능 모델로, 국내 최초로 대규모 심리상담 데이터셋을 체계적으로 구축하여 이를 기반으로 상담 AI 에이전트를 개발한 연구.

- **데이터셋**: CACTUS
  - CBT를 기반으로 설계된 대규모 상담 대화 데이터셋
  - 내담자의 다양한 성격 및 인지적 오류를 고려하여 구체적인 상담 계획을 수립하고 대화를 진행하는 형식으로 구성
  - 거대 언어모델을 활용한 시뮬레이션을 통해 생성
  - 기존 데이터셋 대비 전문성과 현실성을 대폭 향상

- **특징**:
  - 현실적인 상담 시나리오에 최적화
  - 단순 공감에서 벗어나 체계적인 상담 기법을 바탕으로 문제 해결에 초점
  - 기존 상용 챗봇 대비 전문성과 효과성을 향상

### 프로젝트 목적
- 기본적으로 Camel 모델은 **단순한 감정 공감과 상담 대화의 구조적 생성**만 가능한 모델임. 이에 **Dialogue State Tracking(DST)** 기법을 통합하여 내담자의 감정 상태를 더욱 정밀하게 추적하고, 대화의 맥락을 유지함으로써 상담 효과를 향상시킴.
- **RAG**를 활용하여 심리학적 참고 문헌과 서적 데이터를 효율적으로 통합, 상담 AI 에이전트의 전문성을 심화시키고 보다 신뢰성 높은 상담을 가능하게 함.

## 한계점
- **심리학적 전문성의 부족**: 심리학 배경이 부족한 상태에서 심리 서적을 선정함에 따라 일부 데이터의 신뢰성과 적합성이 부족할 가능성이 있음.
- **추후 연구 방향**:
  - 심리학 전공 지식과 전문가 피드백을 기반으로 데이터 검증 및 치료 기법을 다양화.
  - 다양한 심리적 접근법(예: ACT, DBT 등)의 통합을 통해 모델의 적용 범위를 확장.

## 배운 점
- **Agent 기반 LLM 활용의 고도화**: 상담 에이전트에서 LLM의 실질적 활용성을 높이는 방법론을 학습하고 이를 실질적인 구현으로 연결.
- **Dialogue Task 이론 및 응용**:
  - Task-Oriented Dialogue의 핵심 구성 요소인 DST 기법을 학습하고 이론적 이해를 토대로 모델에 성공적으로 통합.
  - 대화의 상태 관리 및 내담자와의 다중턴 상호작용에서 더욱 높은 일관성을 달성.
- **모델 최적화 및 배포**:
  - Camel 모델의 기존 vLLM 구조를 로컬 환경에서 작동 가능하도록 양자화 기술을 적용.
  - Google Colab 환경에서도 실행 가능하도록 최적화하여 학습 및 연구 접근성을 확대.

---




## 기술 흐름도
```plaintext
1. CACTUS 데이터셋 로드
2. Camel 모델 기반 대화 환경 설정
3. DST 모듈 통합 및 상태 추적 강화
4. 심리 서적 데이터를 RAG 기법으로 통합
5. 상담 시뮬레이션 테스트 및 평가
```

## 사용 기술
- **언어 및 프레임워크**: Python, PyTorch, Hugging Face Transformers
- **기술 스택**:
  - Dialogue State Tracking (DST)
  - Retrieval-Augmented Generation (RAG)
  - LLM 양자화 및 최적화
  - Colab 환경 지원 코드 작성

---

## 기대효과 및 결론
- Camel 모델에 DST를 통합하여 내담자의 감정을 정밀하게 추출하고 **공감 능력**을 크게 향상.
- RAG 기법으로 심리 서적 데이터를 통합하여 전문성과 신뢰성 강화.
- Colab 환경에서 운영 가능하도록 코드 최적화, 연구 및 실제 상담 적용 가능성 제시.
- Multi-Modal-Multi-Turn 상담 모델도 구상중.
---

## 참고문헌
- Lee, S., Kim, S., Kim, M., Kang, D., Yang, D., Kim, H., ... & Yeo, J. (2024). CACTUS: towards psychological counseling conversations using cognitive behavioral theory. arXiv preprint arXiv:2407.03103.
- Feng, Y., Lu, Z., Liu, B., Zhan, L., & Wu, X. M. (2023). Towards LLM-driven dialogue state tracking. arXiv preprint arXiv:2310.14970.
- Niu, C., Wang, X., Cheng, X., Song, J., & Zhang, T. (2024). Enhancing Dialogue State Tracking Models through LLM-backed User-Agents Simulation. arXiv preprint arXiv:2405.13037.
- Wu, Y., Dong, G., & Xu, W. (2023). Semantic parsing by large language models for intricate updating strategies of zero-shot dialogue state tracking. arXiv preprint arXiv:2310.10520.
