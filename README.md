# Equivalence Relation Checker

이 Python 모듈은 주어진 관계 \( R \)이 주어진 집합 \( A \)에 대해 동치 관계인지 확인하는 도구입니다. 이 모듈은 다음 세 가지 관계 성질을 검사합니다:

- **반사성**: 모든 \( a \in A \)에 대해 \( (a, a) \in R \)이어야 합니다.
- **대칭성**: 만약 \( (a, b) \in R \)이면 \( (b, a) \in R \)도 성립해야 합니다.
- **추이성**: 만약 \( (a, b) \in R \)이고 \( (b, c) \in R \)이면 \( (a, c) \in R \)도 성립해야 합니다.

## 함수 설명

### `check_reflexive(A, R)`

```python
def check_reflexive(A, R):
    for a in A:
        if (a, a) not in R:
            return False
    return True
