# Mental Health Chatbot
Streamlit 기반 **한국어 심리상담/정신건강 상담 챗봇**입니다.  
사용자 입력을 문장 임베딩으로 변환한 뒤, 사전 구축된 응답 임베딩과 **코사인 유사도**로 가장 적합한 답변을 찾아 대화합니다.

---

## Features
- 한국어 **Sentence-BERT** 임베딩: `jhgan/ko-sroberta-multitask`
- 사전 구축된 응답 임베딩 CSV를 이용한 **빠른 유사도 검색**
- **Streamlit UI** + `streamlit-chat`로 간단한 챗 인터페이스
- 모델/데이터셋 **캐시**(Streamlit `@st.cache_resource`)로 로딩 최적화

---

## Tech Stack
- Python 3.8+
- Streamlit, streamlit-chat  
- pandas, numpy  
- sentence-transformers  
- scikit-learn (코사인 유사도 사용)

---

## Installation

### 1) 가상환경(권장)
```bash
python -m venv .venv
source .venv/bin/activate  # (Windows) .venv\Scripts\activate
