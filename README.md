# equiv_relation_check
# (1)  여기에 전체 코드
def check_reflexive(A, R):
    for a in A:
        if (a, a) not in R:
            return False
    return True

def check_symmetric(R):
    for (a, b) in R:
        if (b, a) not in R:
            return False
    return True

def check_transitive(R):
    for (a, b) in R:
        for (c, d) in R:
            if b == c and (a, d) not in R:
                return False
    return True

def check_equivalence(A, R):
    return check_reflexive(A, R) and check_symmetric(R) and check_transitive(R)

# 예시로 주어진 집합 A와 관계 R
A = {1, 2, 3, 4}
R = {(1, 1), (1, 3), (2, 2), (3, 3), (3, 1), (3, 4), (4, 4), (4, 3)}

# 결과 출력
print("Reflexive:", check_reflexive(A, R))  # True
print("Symmetric:", check_symmetric(R))    # True
print("Transitive:", check_transitive(R))  # False
print("Equivalence:", check_equivalence(A, R))  # False
