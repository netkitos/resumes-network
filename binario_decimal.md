## 🧠 O que é o Sistema Binário

O **sistema binário** é um **sistema numérico de base 2**, usado pelos computadores para representar dados.  
Enquanto o sistema decimal usa **10 dígitos (0 a 9)**, o binário usa apenas **dois símbolos: 0 e 1**.

Cada dígito binário é chamado de **bit** (*Binary Digit*).  
Um grupo de **8 bits** forma um **byte**, e cada posição no número binário tem um **peso** baseado em potências de 2.

📘 **Exemplo de posições binárias (da direita para a esquerda):**

| Bit | 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 |
|-----|---|---|---|---|---|---|---|---|
| Peso (2ⁿ) | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

---

## 💡 Como Funciona o Sistema Binário

Cada posição representa uma **potência de 2**. O valor total é a **soma dos pesos das posições que têm o bit 1**.

📘 **Exemplo:**  
`1101₂`

➡️ Representa:  
`(1 × 8) + (1 × 4) + (0 × 2) + (1 × 1)`  
`= 8 + 4 + 0 + 1`  
`= 13₁₀`

✅ **1101₂ = 13₁₀**

---

## 🔁 Conversão de Binário → Decimal

**Passos:**
1. Escreva o número binário.  
2. Atribua pesos às posições (potências de 2, da direita para a esquerda).  
3. Multiplique cada bit pelo seu peso.  
4. Some todos os resultados.

📘 **Exemplo:**  
`101010₂ = ?`

| Bit | 1 | 0 | 1 | 0 | 1 | 0 |
|-----|---|---|---|---|---|---|
| Peso | 32 | 16 | 8 | 4 | 2 | 1 |
| Cálculo | (1×32) + (0×16) + (1×8) + (0×4) + (1×2) + (0×1) |

➡️ **Resultado: 32 + 8 + 2 = 42₁₀**

✅ **101010₂ = 42₁₀**

---

## 🔁 Conversão de Decimal → Binário

**Método:** divisão sucessiva por 2.

1. Divida o número decimal por 2.  
2. Anote o **resto** (0 ou 1).  
3. Divida o **quociente** novamente por 2.  
4. Continue até o quociente ser 0.  
5. O número binário é formado pelos **restos lidos de baixo para cima**.

📘 **Exemplo:**  
Converter 25₁₀ → binário:

| Divisão | Quociente | Resto |
|----------|------------|--------|
| 25 ÷ 2 | 12 | 1 |
| 12 ÷ 2 | 6 | 0 |
| 6 ÷ 2 | 3 | 0 |
| 3 ÷ 2 | 1 | 1 |
| 1 ÷ 2 | 0 | 1 |

➡️ **Lendo de baixo para cima:** `11001₂`

✅ **25₁₀ = 11001₂**

---

## 🧩 Conversões Rápidas (Binário ↔ Decimal)

| Decimal | Binário | Decimal | Binário |
|----------|----------|----------|----------|
| 0 | 00000000 | 8 | 00001000 |
| 1 | 00000001 | 16 | 00010000 |
| 2 | 00000010 | 32 | 00100000 |
| 3 | 00000011 | 64 | 01000000 |
| 4 | 00000100 | 128 | 10000000 |
| 5 | 00000101 | 255 | 11111111 |

Essas conversões são **fundamentais para entender máscaras de sub-rede e endereçamento IP**, pois cada octeto do IPv4 representa **8 bits (0–255)**.

---

## 🧮 Dica Prática para Redes (CCNA)

Cada **bit** em um octeto vale:

| Bit | Valor |
|-----|--------|
| 1 | 128 |
| 2 | 64 |
| 3 | 32 |
| 4 | 16 |
| 5 | 8 |
| 6 | 4 |
| 7 | 2 |
| 8 | 1 |

🔹 Somando diferentes combinações desses valores, você consegue encontrar **qualquer número entre 0 e 255**, base para **endereços IPv4 e máscaras**.

---

## 🎯 Conclusão

- O **sistema binário** é a linguagem nativa dos computadores.  
- Cada **bit** representa uma **potência de 2**.  
- **Converter entre binário e decimal** é apenas somar ou decompor esses valores.  
- Entender isso é essencial para **endereçamento IP, máscaras de sub-rede e roteamento.**

✨ **Em resumo:**  
> “O binário é o alfabeto da máquina — quem domina ele, entende o idioma das redes.”

---

praticar mais em: https://app.hackone.com.br/courses/downloads/2149689835/ip_addressing_and_subnetting_workbook-pdf

✍️ *Resumo criado para estudos de fundamentos de redes e preparação para o CCNA.*
