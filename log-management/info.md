# 📊 Laboratório: Log Management - LetsDefend

Este repositório contém a documentação prática e a resolução das questões do laboratório de **Log Management** da plataforma **LetsDefend**.

---

## 🎯 Objetivo do Laboratório

Aprender a realizar pesquisas práticas em sistemas de gestão de registros (*Log Management* / SIEM) para:
- Filtrar e identificar endereços IP de origem (`SRC ADDRESS`).
- Analisar tipos de eventos e protocolos (`TYPE`).
- Localizar conexões através de portas de destino (`DEST PORT`) e URLs.

---

## 🛠️ Ferramentas & Conceitos Utilizados

- **Ferramenta:** LetsDefend Log Management
- **Campos de Registos Analisados:**
  - `SRC ADDRESS`: Endereço IP da máquina de origem.
  - `DEST PORT`: Porta de destino do tráfego.
  - `TYPE`: Tipo/protocolo do registo (ex: `dns`, `proxy`).

---

## 📂 Conteúdo

- [Documentação - Laboratório LetsDefend](lab-log-management.md)

---

## 🔍 Metodologia de Pesquisa Utilizada

1. **Leitura da Pergunta:** Identificação do indicador (URL, IP ou Porta).
2. **Filtragem no Painel:** Inserção do valor exato na barra de busca do *Log Management*.
3. **Análise das Colunas:** Verificação das colunas correspondentes para extrair o dado solicitado.
4. **Registo de Evidência:** Captura de ecrã do registo localizado.
