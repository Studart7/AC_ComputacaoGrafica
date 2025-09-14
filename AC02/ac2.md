
---

# Exercícios 

## 1) Translação simples

**Pergunta:** $P(2,3)$ transladado por $(4,-2)$.
**Resposta:** **$P'=(6,1)$** (x aumentou 4; y diminuiu 2).

```python
P = np.array([[2, 3]])
Pp = t(P, (4, -2))
plot_point(P, Pp, "Ex.1 — Translação (4, -2)")
```

---

## 2) Escala uniforme (fator 2)

**Triângulo:** $A(1,1), B(3,1), C(2,4)$.
**Resposta:** **$A'(2,2), B'(6,2), C'(4,8)$**. (coordenadas dobram; comprimentos ×2; área ×4)

```python
tri = np.array([[1,1],[3,1],[2,4]])
tri2 = s(tri, (2, 2))
plot_poly(tri, tri2, "Ex.2 — Escala uniforme ×2")
```

---

## 3) Escala não uniforme $(2,\;0{,}5)$

**Base:** triângulo do Ex. 2.
**Resposta:** **$A'(2,0{,}5), B'(6,0{,}5), C'(4,2)$**. (alonga em x, “achata” em y; área preservada)

```python
tri = np.array([[1,1],[3,1],[2,4]])
tri3 = s(tri, (2, 0.5))
plot_poly(tri, tri3, "Ex.3 — Escala não uniforme (2, 0.5)")
```

---

## 4) Rotação 90° anti-horário (origem)

**Ponto:** $P(1,0)$.
**Resposta:** **$P'=(0,1)$**.

```python
P = np.array([[1, 0]])
Pp = r(P, 90)  # 90° CCW
plot_point(P, Pp, "Ex.4 — Rotação 90° CCW")
```

---

## 5) Rotação de um quadrado 45° horário

**Quadrado:** $A(1,1), B(1,4), C(4,4), D(4,1)$.
**Resposta (aprox.):**
**$A'(1.41,0.00), B'(3.54,2.12), C'(5.66,0.00), D'(3.54,-2.12)$**.

```python
square = np.array([[1,1],[1,4],[4,4],[4,1]])
square_r = r(square, -45)  # 45° horário
plot_poly(square, square_r, "Ex.5 — Rotação 45° CW")
```

---

## 6) Reflexão em relação ao eixo $y$

**Ponto:** $P(2,5)$.
**Resposta:** **$P'=(-2,5)$**.

```python
P = np.array([[2, 5]])
Pp = ry(P)
plot_point(P, Pp, "Ex.6 — Reflexão no eixo y")
```

---

## 7) Reflexão de triângulo em relação ao eixo $x$

**Triângulo:** $A(2,3), B(4,3), C(3,5)$.
**Resposta:** **$A'(2,-3), B'(4,-3), C'(3,-5)$**.

```python
tri = np.array([[2,3],[4,3],[3,5]])
tri_r = rx(tri)
plot_poly(tri, tri_r, "Ex.7 — Reflexão no eixo x")
```

---

## 8) Cisalhamento horizontal $k=2$

**Ponto:** $P(2,3)$.
**Resposta:** **$P'=(8,3)$** (x′ = x + 2y).

```python
P = np.array([[2, 3]])
Pp = shx(P, 2)
plot_point(P, Pp, "Ex.8 — Cisalhamento horizontal k=2")
```

---

## 9) Composição: T(1,−1) → R(90° CCW) → S(2)

**Ponto:** $P(3,2)$.
**Resposta:** **$P'=(-2,8)$**.

```python
P = np.array([[3, 2]])
P1 = t(P, (1, -1))   # (4,1)
P2 = r(P1, 90)       # (-1,4)
P3 = s(P2, (2, 2))   # (-2,8)
plot_point(P, P3, "Ex.9 — T→R→S (resultado final)")
```

---

## 10) Retângulo: T(−2,3) → S(1.5,0.5) → Reflexão em $y$

**Retângulo:** $A(1,1), B(5,1), C(5,3), D(1,3)$.
**Resposta:** **$A'(1.50,2.00), B'(-4.50,2.00), C'(-4.50,3.00), D'(1.50,3.00)$**.

```python
rect = np.array([[1,1],[5,1],[5,3],[1,3]])
rect_t = t(rect, (-2, 3))
rect_s = s(rect_t, (1.5, 0.5))
rect_r = ry(rect_s)
plot_poly(rect, rect_r, "Ex.10 — T(-2,3) → S(1.5,0.5) → Reflexão em y")
```

---

