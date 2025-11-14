# Aplicações Industriais — Capítulo 7 (Root Locus)

## 1. Controle Industrial
O método do Lugar das Raízes é amplamente usado no projeto de:

- controladores PI/PID
- malhas de nível e pressão em reatores
- controle de motores AC e DC
- controle de velocidade e torque em servomotores industriais
- controle de posição em robôs (servodrives)

---

## 2. Ajuste de Controladores via LGR

### ✔ Em plantas químicas (válvulas, pressão e temperatura)
- O LGR permite escolher o ganho ideal sem causar oscilação.
- Ajuda a reduzir o overshoot térmico e economizar energia.

### ✔ Em linhas robotizadas
- O LGR é usado para ajustar controladores **PD / Lead** de servomotores.
- Garantia de resposta rápida sem vibrações.

### ✔ Em motores elétricos (AC Drives / VFD)
- Root Locus determina estabilidade em malhas de corrente e velocidade.

---

## 3. Conexão com Indústria 4.0

### 🧠 APC (Advanced Process Control)
O LGR é base para:
- controle otimizado
- ajuste de malhas PID em processos complexos
- tuning automático

### 🌐 Digital Twins
Simulações no digital twin usam LGR para:
- prever estabilidade
- validar novos controladores antes da implementação real

### 🔗 TI–TO (Integração via PLC/SCADA)
- PLCs usam ajustes de PID baseados em métodos clássicos como LGR
- SCADA registra desempenho e realimenta ajustes automáticos (AI/ML)

---

## 4. Conclusão
O Lugar das Raízes continua sendo uma das técnicas mais intuitivas e robustas para projeto de controladores, mesmo em sistemas industriais modernos conectados à Indústria 4.0.
