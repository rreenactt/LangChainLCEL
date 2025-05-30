# LangChainLCEL
# 🧠 LCEL (LangChain Expression Language)

**LCEL**은 LangChain Expression Language의 약자로, LangChain 프레임워크에서 LLM 기반 애플리케이션을 **선언적** 방식으로 구성하고 실행하기 위한 언어입니다. 복잡한 체인을 간결하게 정의할 수 있으며, 프로토타이핑에서 프로덕션까지 일관된 체인 구성을 지원합니다.

---

## 🔑 핵심 개념

### ✅ 선언적 구성 방식
- '무엇을 할 것인가'에 초점을 맞춰 체인을 정의
- 실행 세부사항은 LangChain이 처리

### 🔗 Runnable 인터페이스
- 모든 LCEL 구성요소는 `Runnable`을 구현
- 주요 메서드: `invoke()`, `batch()`, `stream()`

### ➕ 파이프 연산자 (`|`)
- 체인의 각 단계는 `|` 연산자를 통해 연결
```python
chain = prompt | model | output_parser