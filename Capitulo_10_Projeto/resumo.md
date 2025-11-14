# Capítulo 10 — Projeto de Sistemas de Controle com Realimentação

## 1. Introdução
O projeto de sistemas de controle busca **atender especificações de desempenho**, tais como:
- rapidez,
- amortecimento,
- overshoot,
- erro em regime permanente,
- robustez.

Para isso, utilizamos controladores e compensadores que modificam a posição dos polos e zeros do sistema e ajustam sua resposta.

---

## 2. Especificações de Desempenho

### 2.1 Resposta transitória
Relacionada a:
- **overshoot (Mp)**  
- **tempo de acomodação (ts)**  
- **fator de amortecimento (ζ)**  
- **frequência natural (ωn)**

Relações úteis (para 2ª ordem):

$$
M_p = e^{-\pi\zeta / \sqrt{1-\zeta^2}}
$$


$$
t_s \approx \frac{4}{\zeta \omega_n}
$$

---

## 3. Tipos de Controladores

### 3.1 Controlador Proporcional (P)
Aumenta o ganho, melhora o erro estacionário, porém pode prejudicar a estabilidade.

### 3.2 Controlador PI


$$
C(s) = K\left(1 + \frac{1}{T_i s}\right)
$$

Elimina erro estacionário para degrau.

### 3.3 Controlador PD

$$
C(s) = K(1 + T_d s)
$$

Melhora velocidade e reduz overshoot.

### 3.4 Controlador PID

$$
C(s) = K\left(1 + \frac{1}{T_i s} + T_d s\right)
$$

O mais usado industrialmente.

---

## 4. Compensadores Clássicos

### 4.1 Compensador Lead
Aumenta a rapidez, desloca polos para a esquerda.

$$
C(s)=\frac{s+z}{s+p}, \quad z<p
$$

### 4.2 Compensador Lag
Melhora erro estacionário sem modificar muito a dinâmica.

$$
C(s)=\frac{s+z}{s+p}, \quad z>p
$$

### 4.3 Lead–Lag
Combina as duas melhorias:
- rapidez (lead)
- precisão (lag)

---

## 5. Projeto no Domínio do Tempo (LGR)
O método do Lugar das Raízes é usado para:
- posicionar polos desejados,
- ajustar ganho K,
- adicionar zeros (PD/lead),
- melhorar amortecimento.

---

## 6. Projeto no Domínio da Frequência
(diagramas de Bode)

Permite:
- garantir **margem de fase**
- garantir **robustez**
- projetar compensadores usando retificação de fase

Especificações típicas:
- Margem de Fase ≥ 45°
- Margem de Ganho ≥ 6 dB

---

## 7. Sistema em Malha Fechada
A função de transferência final é:

$$
T(s)=\frac{C(s)G(s)}{1 + C(s)G(s)}
$$

O objetivo é deslocar polos para regiões onde o sistema:
- é estável,
- apresenta resposta rápida,
- e possui baixo erro estacionário.

---

## 8. Conclusão
O projeto de sistemas de controle integra:
- análise no tempo,
- análise na frequência,
- métodos gráficos (LGR),
- controladores P, PI, PD, PID,
- compensadores clássicos.

Tudo isso permanece essencial na automação industrial moderna e serve como base para APC, MPC e estratégias inteligentes.
