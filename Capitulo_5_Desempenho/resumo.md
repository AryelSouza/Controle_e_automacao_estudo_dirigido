# Capítulo 5 — Desempenho de Sistemas de Controle com Realimentação

## 1. Introdução
O **desempenho de um sistema de controle** está relacionado à qualidade da resposta do sistema quando sujeito a entradas ou perturbações.  
Nesta análise, avaliamos **rapidez, precisão e estabilidade** — três pilares de um bom projeto de controle.

O desempenho pode ser medido tanto no **domínio do tempo** (resposta transitória e regime permanente) quanto no **domínio da frequência** (magnitude e fase).

---

## 2. Resposta Transitória
É o comportamento do sistema **logo após** a aplicação de uma entrada (ex: degrau).  
Para sistemas de 2ª ordem, a resposta depende de dois parâmetros:

\[
\omega_n = \text{frequência natural não amortecida}
\]
\[
\zeta = \text{fator de amortecimento}
\]

A forma geral é:

\[
T(s) = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}
\]

### Parâmetros importantes:
| Parâmetro | Símbolo | Significado |
|------------|----------|-------------|
| Tempo de subida | \(t_r\) | tempo para atingir 90% do valor final |
| Tempo de pico | \(t_p\) | instante do primeiro pico máximo |
| Tempo de acomodação | \(t_s\) | tempo para estabilizar dentro de ±2% |
| Sobressinal máximo | \(M_p\) | quanto o sinal ultrapassa o valor final |

---

## 3. Erro de Regime Permanente
O **erro de regime permanente** (ess) mede a diferença entre a saída e a referência após o sistema se estabilizar.  
Depende do tipo de sistema e do tipo de entrada (degrau, rampa, parábola...).

| Tipo do Sistema | Constante | Entrada Degrau | Entrada Rampa |
|------------------|------------|----------------|----------------|
| Tipo 0 | \(K_p\) | erro finito | erro infinito |
| Tipo 1 | \(K_v\) | erro zero | erro finito |
| Tipo 2 | \(K_a\) | erro zero | erro zero |

---

## 4. Trade-offs de Projeto
Melhorar o desempenho envolve **compromissos**:

- Aumentar o ganho \(K\) → reduz o erro estacionário, mas pode causar **oscilação**.  
- Aumentar o amortecimento \(\zeta\) → reduz o sobressinal, mas **torna a resposta mais lenta**.  
- Projetar compensadores → balancear rapidez, precisão e estabilidade.

---

## 5. Realimentação e Robustez
A realimentação:
- **Reduz sensibilidade** a variações de parâmetros.
- **Aumenta robustez** a ruídos e distúrbios.
- **Modifica a resposta transitória**, melhorando o desempenho global.

---

## 6. Avaliação de Desempenho
Métodos típicos:
- Resposta ao degrau
- Erro em regime permanente
- Lugar das raízes
- Diagramas de Bode

Ferramentas como `control.step_response()` e `control.info()` em Python permitem medir esses parâmetros automaticamente.

---

## 7. Conclusão
Analisar o desempenho é essencial para garantir que um sistema de controle atenda a requisitos industriais: **rapidez, estabilidade e precisão**.  
Na **Indústria 4.0**, o desempenho é monitorado continuamente em tempo real por sistemas **APC, MES e Digital Twin**, permitindo **autoajuste dinâmico e otimização contínua**.
