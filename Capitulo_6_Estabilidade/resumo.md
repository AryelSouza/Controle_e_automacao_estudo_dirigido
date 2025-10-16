# Capítulo 6 — Estabilidade de Sistemas Lineares com Realimentação

## 1. Introdução
A **estabilidade** é a propriedade fundamental de um sistema de controle.  
Um sistema é estável se, ao ser perturbado, sua resposta tende a retornar a um estado de equilíbrio finito com o tempo.  
Na prática, estabilidade garante **segurança e previsibilidade**.

---

## 2. Definições Fundamentais
- **Estável** → a resposta permanece limitada para qualquer entrada limitada (Bounded-Input Bounded-Output, BIBO).  
- **Instável** → a saída cresce indefinidamente.  
- **Marginalmente estável** → oscila indefinidamente (sem crescer nem decrescer).

Matematicamente, a estabilidade depende da **posição dos polos** da função de transferência \( T(s) \).

---

## 3. Critério de Estabilidade
Para um sistema linear com função de transferência:

$$
T(s) = \frac{N(s)}{D(s)} = \frac{N(s)}{s^n + a_1 s^{n-1} + a_2 s^{n-2} + \dots + a_n}
$$

O sistema é **estável** se **todos os polos (raízes de D(s))** estiverem no **semiplano esquerdo** do plano complexo (parte real negativa).

---

## 4. Critério de Routh-Hurwitz
Permite verificar a estabilidade **sem calcular explicitamente os polos**.

Para um polinômio característico:

$$
D(s) = a_0 s^n + a_1 s^{n-1} + \dots + a_n
$$

Construímos a **tabela de Routh**, e o sistema é estável se **todos os elementos da primeira coluna forem positivos**.

### Exemplo:

$$
D(s) = s^3 + 2s^2 + 3s + 5
$$

→ Primeira coluna de Routh: [1, 2, 2, 5] → todos positivos → **estável**.

---

## 5. Relação com o Lugar das Raízes
A posição dos polos em função do ganho $$\(K\)$$ pode ser estudada pelo **método do Lugar das Raízes** (Capítulo 7).  
À medida que $$\(K\)$$ aumenta, os polos se movem e podem atravessar o eixo imaginário — indicando **perda de estabilidade**.

---

## 6. Estabilidade e Realimentação
A realimentação negativa melhora a precisão, mas **pode afetar a estabilidade**.  
Um ganho excessivo pode deslocar polos para o semiplano direito, tornando o sistema instável.

---

## 7. Análise via Resposta Temporal
Na resposta ao degrau:
- Se a saída tende a um valor finito → **estável**.  
- Se oscila indefinidamente → **marginalmente estável**.  
- Se cresce sem limite → **instável**.

---

## 8. Estabilidade Relativa
Mesmo sistemas estáveis podem ter **respostas lentas ou muito oscilatórias**.  
A análise de estabilidade relativa mede **o quão distante os polos estão do eixo imaginário** — ou seja, **a margem de segurança**.

---

## 9. Conclusão
A estabilidade é a **condição mínima** para qualquer sistema de controle.  
Na Indústria 4.0, a estabilidade está diretamente ligada à **confiabilidade** e **segurança funcional**, especialmente em sistemas críticos como **SIS (Safety Instrumented Systems)** e **DCS (Distributed Control Systems)**.
