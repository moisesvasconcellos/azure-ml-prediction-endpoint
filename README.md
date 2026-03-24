# 🚀 Projeto de Machine Learning no Azure (Endpoint de Previsão)

Este projeto demonstra a criação de um modelo de Machine Learning no Azure Machine Learning e sua publicação como um serviço acessível via API REST.

---

## 🎯 Objetivo

Criar um modelo de previsão utilizando Azure Machine Learning e disponibilizá-lo através de um endpoint para consumo em aplicações externas.

---

## 🛠️ Tecnologias Utilizadas

- Azure Machine Learning
- AutoML (Machine Learning Automatizado)
- Python (ambiente gerado automaticamente)
- API REST
- JSON
- GitHub

---

## 📊 Etapas do Projeto

### 1. Criação do Workspace
Foi utilizado o Azure Machine Learning Studio para criação do ambiente de trabalho.

---

### 2. Treinamento do Modelo
Utilizando o AutoML, foi criado um modelo de previsão baseado em dados estruturados.

---

### 3. Implantação do Modelo
O modelo foi publicado através de um:

- Endpoint em tempo real (Real-time endpoint)
- Máquina virtual: `Standard_DS2_v2`
- Instância: 1 (otimizado para custo)

---

### 4. Criação do Endpoint
O modelo foi exposto via API REST, permitindo integração com outras aplicações.

Exemplo de endpoint:


https://seu-endpoint.australiaeast.inference.ml.azure.com/score

---

### 5. Teste do Modelo

Foi realizado teste diretamente no Azure utilizando um payload JSON.

---

## 📥 Exemplo de Requisição (JSON)

```json
{
  "input_data": {
    "columns": [
      "day",
      "mnth",
      "year",
      "season",
      "holiday",
      "weekday",
      "workingday",
      "weathersit",
      "temp",
      "atemp",
      "hum",
      "windspeed"
    ],
    "index": [0],
    "data": [
      [1, 1, 1, 1, 0, 6, 0, 2, 0.34, 0.36, 0.80, 0.16]
    ]
  }
}

Resultado

O modelo retornou a seguinte previsão:

[467.3258696393905]

Aprendizados

Durante este projeto foi possível compreender:

Como treinar modelos com AutoML
Como publicar modelos como API
Estrutura de entrada de dados (JSON)
Importância da consistência dos dados
Diagnóstico de erros via logs
Deploy de modelos em ambiente cloud

Observações Importantes
O endpoint gera custo enquanto estiver ativo
Recomenda-se excluir o endpoint após uso

Conclusão

Este projeto demonstra na prática como transformar um modelo de Machine Learning em um serviço real na nuvem, pronto para ser consumido por aplicações.

Autor

Desenvolvido por Moisés Vasconcellos

