# 💰 Caderno de Dívidas com IA

Este projeto implementa um caderno simples para gerenciar dívidas, utilizando Inteligência Artificial (IA) para interpretar comandos em linguagem natural e realizar as operações.

## 💡 Origem e Motivação do Projeto

Este Caderno de Dívidas com IA surgiu de uma necessidade real e pessoal: **simplificar o trabalho do meu pai**. Atualmente, ele gerencia uma série de contas e dívidas de forma manual em um caderno físico, o que envolve fazer contas grandes e complexas à mão.

O objetivo principal deste projeto é **substituir esse processo manual e trabalhoso por uma solução rápida e simples no celular**, permitindo que ele registre novas dívidas, visualize resumos e marque pagamentos apenas digitando frases simples, sem precisar lidar diretamente com os números e cálculos. É um passo para trazer mais agilidade e praticidade para o dia a dia de trabalho dele.

## ✨ Funcionalidades

O projeto permite gerenciar dívidas através de comandos em linguagem natural:

* **Anotar novas dívidas:** Registrar o valor e a pessoa que deve, além de um motivo (opcional).
* **Mostrar resumo:** Visualizar o total de dívidas pendentes para cada pessoa.
* **Marcar pagamento:** Registrar pagamentos parciais ou marcar dívidas como totalmente pagas para uma pessoa específica.
* **Ver individual:** Listar todas as dívidas (pendentes e pagas) de uma pessoa com detalhes.
* **Obter ajuda:** Ver uma lista dos comandos que o assistente compreende.

## 🧠 Integração com IA

O projeto utiliza o modelo **Gemini 2.0 Flash** da Google para interpretar as frases digitadas pelo usuário. A IA analisa a entrada e identifica a **intenção** (o que o usuário quer fazer, como anotar, mostrar resumo, marcar pago, etc.) e extrai as **informações relevantes** (como nome da pessoa, valor, motivo) para que o programa possa executar a ação correta.

## 🚀 Como Rodar o Projeto no Google Colab

Este projeto foi desenvolvido para rodar no ambiente do Google Colab, o que facilita a execução sem necessidade de instalações complexas na máquina local (além da configuração da API Key).

Para rodar o notebook:

1.  **Abra o Notebook no Google Colab:**
    * Vá para a página deste repositório no GitHub.
    * Procure pelo arquivo `Projeto_Caderno_de_Dívidas.ipynb`
    * Clique no nome do arquivo para visualizar o conteúdo no GitHub.
    * Procure por um botão **"Open in Colab"** perto do topo da página. Clique nele.
    * **Caso o botão "Open in Colab" não apareça:** Vá diretamente para [https://colab.research.google.com/](https://colab.research.google.com/), clique em `Arquivo` > `Abrir notebook`, selecione a aba `GitHub`, pesquise por `PouDev/Projeto-Caderno-de-Di` e selecione o arquivo `.ipynb`.

2.  **Configure a API Key do Gemini:**
    * Você precisará de uma chave de API para o modelo Gemini. Obtenha uma no Google AI Studio ([https://aistudio.google.com/](https://aistudio.google.com/)).
    * No Google Colab, com o notebook aberto, clique no ícone de **chave (Secrets)** no lado esquerdo da tela.
    * Clique em `Adicionar novo Segredo`.
    * Crie um segredo com o nome **`GEMINI_API_KEY`** (exatamente este nome).
    * No campo "Valor", cole a chave de API que você obteve no Google AI Studio.
    * Certifique-se de que o "Acesso ao notebook" para este segredo está ativado.

3.  **Rode as Células do Notebook:**
    * Rode as células do notebook na seguinte ordem:
        * Célula de Inicialização (`caderno_dividas = []`)
        * Célula de Instalação (`!pip install ...`)
        * Célula de Configuração do Modelo IA (Onde configura a API Key e o modelo `model`)
        * Célula com as Definições das Funções do Caderno
        * Célula com o Loop Principal de Interação (o loop `while True:`)

4.  **Interaja com o Caderno:**
    * Após rodar a última célula (o loop principal), você poderá interagir com o assistente digitando seus comandos em linguagem natural na **área de entrada de texto que aparece abaixo da célula** no próprio ambiente do Google Colab e apertando Enter.
    * Para sair do programa, digite `sair` quando solicitado.

## 📚 Bibliotecas Utilizadas

* `google-generativeai`: Para interagir com os modelos Gemini.
* `python-dotenv`: (Opcional no Colab com Secrets) Para carregar variáveis de ambiente.

---
Espero que gostem, foi trabalhoso mas é algo que irei melhorar e realmente irei usar no meu dia a dia e no do meu pai
