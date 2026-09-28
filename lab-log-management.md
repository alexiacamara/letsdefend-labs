# 📊 Laboratório: Log Management - LetsDefend

## 🎯 Objetivo
Desenvolver a habilidade prática de investigar eventos de segurança no painel de **Log Management**. O foco é utilizar Indicadores de Comprometimento (IOCs) fornecidos pelos alertas do SIEM — como URLs, portas e endereços IP — para filtrar a base de logs, analisar as colunas de dados e identificar a origem e o protocolo das atividades analisadas. <br> <br>
A plataforma informou que o alerta veio de um IP cuja a URL é `https://github.com/apache/flink/compare`. O objetivo é encontrar qual endereço IP de origem inseriu essa URL e qual é o tipo de log que possui um número de porta de destino de `52567`e um endereço IP de origem de `8.8.8.8`


## 🔍 Processo de Investigação

### Investigação por URL
No painel de **Log Management**, o primeiro passo foi pesquisar a URL fornecida pela plataforma: `https://github.com/apache/flink/compare`.

<img width="1561" height="241" alt="log github" src="https://github.com/user-attachments/assets/9d6ce914-fa7d-4bdf-a350-af488aa46630" /> <br>
<img width="1537" height="282" alt="log github 2" src="https://github.com/user-attachments/assets/f2369d11-4556-49e2-b603-aa65aeeff2e1" /> <br>


* **Endereço IP de Origem encontrado:** `172.16.17.54`

---

### Investigação por IP e Porta
Para descobrir o tipo de log que possui a porta de destino `52567` e o IP de origem `8.8.8.8`:

1. A pesquisa inicial foi feita com o número da porta `52567`, retornando dois resultados e apenas um correspondia à porta `52567`.
<img width="1567" height="313" alt="image" src="https://github.com/user-attachments/assets/ce042473-93e3-454c-a796-5d1bad5e56a5" /> <br>

2. Se buscar pelo `8.8.8.8` terá mais IPs pois também aparece o `8.8.8.8` como destino e não é o que o exercício da plataforma pede:
<img width="1555" height="390" alt="image" src="https://github.com/user-attachments/assets/8e9c9351-1f4e-42cf-83ea-9a89f44b5c32" /> <br> <br>

* **Tipo de log:** `DNS`. <br>
O log indica um **Response A**, que é a resposta da consulta DNS mapeando o domínio para um endereço IPv4. O SIEM identifica como DNS porque a porta 53 é exclusiva para esse tipo. Quando um sistema (ou um SIEM) vê tráfego passando pela porta 53, ele já sabe imediatamente que ali está ocorrendo uma consulta ou resposta de DNS.



