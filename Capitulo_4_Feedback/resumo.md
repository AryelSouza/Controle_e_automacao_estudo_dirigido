# Capítulo 4 — Características de Sistemas de Controle com Realimentação

## 1. Introdução
Um **sistema de controle com realimentação (feedback)** compara a saída desejada com a saída real do sistema e ajusta automaticamente o sinal de entrada para corrigir erros.  
A realimentação é o princípio fundamental da automação industrial moderna.

## 2. Estrutura Básica de um Sistema de Controle
[Diagrama conceitual]

Entrada desejada → [Controlador] → [Planta] → Saída medida



↑________________________________________↓


Realimentação (Sensor)


### Elementos principais
- **Controlador (C(s))**: gera a ação de controle (ex: PID, PI, PD)
- **Planta (G(s))**: representa o processo físico (motor, válvula, robô)
- **Sensor**: mede a saída real
- **Realimentação (H(s))**: converte a saída em sinal de comparação

## 3. Função de Transferência com Realimentação

O sistema de malha fechada é representado por:

$$
T(s) = \frac{C(s)G(s)}{1 + C(s)G(s)H(s)}
$$

A realimentação altera:
- **Ganho** → afeta a precisão
- **Resposta transitória** → pode reduzir o tempo de estabilização
- **Estabilidade** → depende do sinal da realimentação

## 4. Efeitos da Realimentação

| Característica | Efeito da Realimentação |
|-----------------|--------------------------|
| Estabilidade    | Pode melhorar (reduz erro) ou piorar (instabilizar) |
| Precisão        | Reduz o erro de regime permanente |
| Sensibilidade   | Diminui a influência de perturbações |
| Ganho efetivo   | Menor, porém mais robusto |

## 5. Erro de Regime Permanente
Depende do tipo de entrada e da **constante de erro** do sistema.

| Tipo de sistema | Entrada degrau | Entrada rampa |
|------------------|----------------|----------------|
| Tipo 0 | erro ≠ 0 | erro → ∞ |
| Tipo 1 | erro = 0 | erro ≠ 0 |
| Tipo 2 | erro = 0 | erro = 0 |

## 6. Realimentação Negativa vs Positiva
- **Negativa** → reduz erro e ruído; é a mais usada.
- **Positiva** → tende a aumentar o erro e pode causar instabilidade (usada em osciladores).

## 7. Benefícios e Limitações
### Benefícios
- Correção automática de erros
- Menor sensibilidade a perturbações externas
- Melhora da precisão

### Limitações
- Custo e complexidade maiores
- Pode reduzir a estabilidade
- Requer sensores confiáveis e calibrados

## 8. Conclusão
A realimentação é a base do **controle automático moderno** e um dos pilares da **Indústria 4.0**, pois permite sistemas autônomos, adaptativos e integrados digitalmente.
