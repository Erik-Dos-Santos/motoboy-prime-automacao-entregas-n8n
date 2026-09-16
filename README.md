
# 🏍️ Motoboy Prime - Automação Logística de Entregas com n8n

O **Motoboy Prime** é uma solução de automação logística desenvolvida no n8n para otimizar o processo de cotação, cálculo de rotas e registro financeiro de entregas urbanas. A partir de comandos simples no Telegram, o sistema processa endereços, calcula a melhor rota via API e registra as informações automaticamente no Google Sheets.

---

## 🛠️ Tecnologias & Ferramentas
* **n8n (Self-Hosted/Local):** Orquestração e automação de todo o fluxo de dados.
* **Telegram Bot API:** Interface principal para envio e recebimento de requisições.
* **Google Routes API:** Geolocalização, cálculo preciso de distâncias (metros) e tempos de percurso.
* **Python:** Lógica de negócio para otimização e seleção automática da menor rota encontrada.
* **JavaScript:** Truncamento, formatação de dados e adequação para moeda local (BRL).
* **Google Sheets:** Banco de dados relacional leve para registro de histórico e controle de caixa.

---

## 📌 Funcionalidades Principais
* 🤖 **Atendimento Via Bot:** Interface no Telegram rápida para entrada de endereços de origem e destino.
* ⚡ **Algoritmo Otimizador em Python:** Filtra automaticamente a rota de menor quilometragem entre as opções retornadas pela API.
* 💰 **Precificação Automática:** Aplica taxa por km rodado e formata o valor no padrão de moeda brasileiro (`R$ X,XX`).
* 📊 **Persistência de Dados:** Gravação automática da data, distância em KM e valor calculado em planilha do Google Sheets.
* 🛡️ **Segurança de Credenciais:** Separação total da lógica do fluxo em relação às chaves e tokens de acesso.

---

## 🏗️ Arquitetura do Fluxo
<img width="737" height="218" alt="Arquitetura do Fluxo" src="https://github.com/user-attachments/assets/f8b9bb78-ec07-425a-9035-9bf715d0eabd" />
                                                
## 📋 Como Executar o Projeto

1. **Faça uma cópia da Planilha Modelo:**
 👉 [**Clique aqui para criar uma cópia da Planilha Modelo**](https://docs.google.com/spreadsheets/d/1KTIt7-Td3lfZmpUESbDWiWd57XXwntnOHC4nY60eBE8/copy)

> **Nota:** Certifique-se de estar conectado à sua conta do Google ao clicar no link para que a cópia seja salva diretamente no seu Drive.

2. **Importe o Fluxo no n8n:**
   * Baixe o arquivo `workflow.json` deste repositório.
   * No n8n, crie um novo workflow e selecione **Import from File**.

3. **Configure as Credenciais:**
   * Conecte sua conta do **Telegram Bot API**.
   * Conecte suas credenciais do **Google Sheets API** e substitua o ID da planilha nos nós pelo ID da sua cópia.
