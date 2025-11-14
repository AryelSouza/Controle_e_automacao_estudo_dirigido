# Capítulo 13 — Sistemas de Controle Digital

## 1. Introdução
O controle digital utiliza controladores implementados em:
- PLCs,
- microcontroladores,
- sistemas embarcados,
- controladores distribuídos (DCS),
- sistemas SCADA e IIoT.

Ele opera em **tempo discreto**, com sinais definidos apenas em instantes múltiplos do período de amostragem.

---

## 2. Sinal Amostrado

Um sinal contínuo \( x(t) \) torna-se um sinal discreto por:

$$
x[k] = x(kT)
$$

Onde:
- \( T \) = período de amostragem  
- \( k \) = índice discreto  

---

## 3. Transformada Z

A transformada Z é definida por:

$$
X(z) = \sum_{k=0}^{\infty} x[k] \, z^{-k}
$$

A ligação com a transformada de Laplace é:

$$
z = e^{sT}
$$

---

## 4. Função de Transferência Digital

Um sistema digital é descrito por:

$$
G(z) = \frac{Y(z)}{U(z)}
$$

Assim como sistemas contínuos, controladores digitais também são funções de transferência no domínio Z.

---

## 5. Discretização de Sistemas Contínuos

Para aplicar controle digital em uma planta contínua, utiliza-se a discretização.

### 5.1 Métodos comuns
- **ZOH (Zero-Order Hold)** — mais utilizado
- **Tustin (bilinear)**
- Aproximação para frente
- Aproximação para trás

---

## 6. Controladores Digitais

### 6.1 PID Digital (forma incremental)

O PID discreto pode ser escrito como:

$$
u[k] = u[k-1]
+ K_p (e[k] - e[k-1])
+ K_i T e[k]
+ \frac{K_d}{T} (e[k] - 2e[k-1] + e[k-2])
$$

### 6.2 Compensadores digitais
- Lead digital  
- Lag digital  
- Lead–Lag  
- Filtros digitais (FIR/IIR)

---

## 7. Estabilidade Digital

Sistemas discretos são **estáveis** quando todos os polos satisfazem:

$$
|z_i| < 1
$$

Isto é: todos os polos devem estar **dentro do círculo unitário** no plano Z.

---

## 8. Projeto Digital

### 8.1 Regras práticas de escolha do período de amostragem

- \( T_s \) deve ser 5 a 20 vezes menor que a dinâmica dominante.  
- Frequência de amostragem deve obedecer:

$$
f_s > 2 f_{\text{max}}
$$

(critério de Nyquist)

---

## 9. Implementação em PLCs e Controladores Industriais

Controladores digitais reais utilizam:
- amostragem determinística,
- blocos PID nativos,
- filtros anti-ruído,
- limites de saturação e anti-windup.

São aplicados em:
- TIA Portal (Siemens),
- Studio 5000 (Rockwell),
- Codesys,
- Beckhoff TwinCAT.

---

## 10. Conclusão
Controle digital é essencial para automação industrial moderna, integração TI–TO, IIoT, Digital Twins e Indústria 4.0.  
Ele permite:
- supervisão em rede,
- controle distribuído,
- comunicação via OPC-UA/MQTT,
- análise em nuvem,
- otimização em tempo real.
