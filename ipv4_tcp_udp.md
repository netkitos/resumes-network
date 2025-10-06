# 🌐 IPv4, DHCP, DNS, TCP e UDP — Resumo de Redes

## 🧩 IPv4

O **IPv4** é um **protocolo da camada de rede** (camada 3 do modelo OSI).  
Sua função é **enviar dados do device A para o device B** em uma rede.

Mas se já existe o **endereçamento MAC**, por que usar o **IPv4**?

👉 Porque o **endereçamento MAC é físico**, e os **roteadores não conseguem ler** endereços físicos de máquinas que estão em outras redes (por exemplo, em outro país).  
Por isso existe o **endereçamento IP**, que permite que os dispositivos se conectem e troquem dados através da Internet.

### 🧠 Resumindo:

- O **endereço MAC** é como o **número de série de uma placa de rede** — identifica o **dispositivo físico**, mas **só é usado dentro da mesma LAN**, onde os quadros Ethernet circulam.  
- O **IPv4** é um **endereço lógico**, que identifica **um ponto de conexão na Internet**. Ele permite **rotear pacotes entre redes diferentes**, **saltando entre roteadores** até chegar ao destino — como um **endereço postal completo** que o correio entende.

---

## ⚙️ Tipos de Endereçamento IPv4

### 🔸 Estático
O **endereço IPv4 estático** é configurado **manualmente** pelo usuário.  
Exemplo: `192.168.10.1`

Ideal para **servidores**, **roteadores** e dispositivos que precisam manter o **mesmo IP sempre**.

### 🔸 Dinâmico (DHCP)

O **DHCP** (*Dynamic Host Configuration Protocol*) **atribui IPs automaticamente** aos dispositivos quando entram na rede.

📘 **Função:** distribuir endereços IP sem precisar configurar manualmente cada equipamento.

**Portas padrão:**  
- Servidor DHCP → **porta 67**  
- Cliente DHCP → **porta 68**

---

## 🌍 DNS (Domain Name System)

Imagina ter que digitar o IP `142.250.190.68` para acessar o Google 😅  
Seria impraticável!  
O **DNS** resolve isso, traduzindo nomes como `www.google.com` em **endereços IP**.

### 🔹 Como funciona o processo DNS

1. O dispositivo pergunta: “Qual o IP de `www.cisco.com`?”  
   A consulta vai para o **servidor DNS configurado** (via DHCP ou manualmente).  
2. Se o servidor não souber, ele consulta os **servidores raiz (root)**.  
   - Estes apontam para os **servidores de domínio de topo (TLD)** — `.com`, `.org`, etc.  
3. O TLD indica os **servidores autoritativos** do domínio `cisco.com`.  
4. O servidor autoritativo responde com o IP verdadeiro.  
5. O IP é **armazenado em cache** (no PC ou roteador) para acelerar consultas futuras.

---

## 🚦 TCP (Transmission Control Protocol)

O **TCP** é um **protocolo de transporte confiável**, criado para garantir que os dados enviados de um **device A** cheguem **completos, sem erros e na ordem correta** ao **device B**.

Antes de transmitir, ele **cria uma conexão** entre remetente e destinatário — por isso é chamado de **orientado à conexão** (*connection-oriented*).

Durante a comunicação, o TCP:
- **Confirma cada pacote recebido** (ACK — *Acknowledgment*),
- **Controla o ritmo de envio** (fluxo),
- **Retransmite pacotes perdidos**.

### 📦 Principais características:
- 🔗 Orientado à conexão (*3-way handshake*)  
- ✅ Confiável (confirmação e retransmissão)  
- 🔢 Ordenado (mantém a sequência dos dados)  
- ⚙️ Controle de fluxo e congestionamento  
- 🐢 Mais lento que UDP, mas muito mais seguro  

### 🔍 Exemplos de aplicações que usam TCP:
HTTP/HTTPS, FTP, SSH, Telnet, SMTP, POP3 — tudo que **não pode perder dados**.

---

## ⚡ UDP (User Datagram Protocol)

O **UDP** é um **protocolo de transporte não orientado à conexão** (*connectionless protocol*).  
Ele envia dados **diretamente**, **sem criar conexão** e **sem confirmar a entrega**.

📘 **Em outras palavras:**
> O UDP entrega os dados o mais rápido possível, mas **não garante entrega, ordem nem integridade**.

É como **enviar uma carta sem pedir confirmação de recebimento** — rápido, mas sem garantias.

### 💬 Aplicações típicas do UDP

Usado quando **velocidade > confiabilidade**, como em:
- 🎥 **Streaming de vídeo/áudio (YouTube, VoIP, IPTV)**  
- 🎮 **Jogos online em tempo real**  
- 🌐 **DNS (consultas rápidas)**  
- 📂 **TFTP (Trivial File Transfer Protocol)**

---

## 🧭 Resumo geral

| Protocolo | Tipo de Conexão | Confiabilidade | Ordem | Velocidade | Exemplos |
|------------|-----------------|----------------|--------|-------------|-----------|
| **TCP** | Connection-oriented | Alta | Mantida | Mais lenta | HTTP, FTP, SSH |
| **UDP** | Connectionless | Baixa | Não garantida | Mais rápida | DNS, VoIP, Jogos |

---

✍️ *Resumo elaborado para estudos de redes e CCNA — Feito por Lucas Miguel.*
