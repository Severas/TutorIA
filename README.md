# 📘 Tutorial de Integração do Google Gemini (IA) no Moodle

Este guia explica como configurar o Google Gemini no Moodle para oferecer tutoria inteligente, feedback automático, geração de conteúdo educacional e recomendações personalizadas aos estudantes.

---

## 🔧 Pré-requisitos

* **Versão do Moodle**: 4.5 ou superior (recomendado Moodle 5.0+).
* **Acesso administrativo** ao Moodle.
* Conta Google.
* **Chave de API do Gemini** obtida no Google AI Studio.
* Servidor Moodle com acesso à internet para chamadas externas de API.

---

## 📥 Obtenção da Chave de API Gemini

1. Acesse o Google AI Studio.
2. Faça login com sua conta Google.
3. Clique em **Get API Key**.
4. Crie uma nova chave de API.
5. Copie e armazene a chave em local seguro.

A API do Gemini oferece uma camada gratuita adequada para desenvolvimento, testes acadêmicos e prototipação.

---

## 📥 Instalação do Plugin de IA no Moodle

O Moodle 5.x possui suporte nativo para integração com provedores de IA através do framework de IA da plataforma.

1. Acesse o Moodle como administrador.

2. Vá em:

   **Site administration > General > AI**

3. Instale um plugin compatível com APIs externas de IA, caso necessário.

4. Após a instalação, configure o Gemini como provedor de IA.

---

## ⚙️ Configuração da API Gemini

1. No painel administrativo, acesse:

   **Site administration > General > AI**

2. Clique em **AI Providers**.

3. Adicione um novo provedor.

4. Configure:

   * **Provider Name:** Google Gemini
   * **API Key:** sua chave gerada no Google AI Studio
   * **Model:** gemini-2.5-flash (recomendado para testes) ou modelo mais recente disponível

5. Salve as configurações.

---

## 🚀 Habilitar Funcionalidades

No menu **AI Placements**, escolha onde o Gemini ficará disponível:

### Editor de Texto

Permite:

* Gerar resumos.
* Reescrever conteúdos.
* Simplificar textos complexos.
* Criar explicações complementares.

### Atividades

Permite:

* Feedback automático.
* Sugestões de melhoria em tarefas.
* Correções preliminares.

### Painel do Professor

Permite:

* Resumos de desempenho.
* Identificação de dificuldades frequentes.
* Apoio na elaboração de avaliações.

---

## 💬 Criando um Chatbot Educacional com Gemini

Uma das aplicações mais interessantes é criar um chatbot acadêmico integrado ao Moodle.

### 1. Definir o Papel do Assistente

O chatbot pode atuar como:

* Tutor virtual.
* Assistente de estudos.
* Monitor de disciplina.
* Orientador de navegação na plataforma.

### 2. Configurar os Locais de Atendimento

Disponibilize o chatbot em:

* Fóruns.
* Página inicial do curso.
* Blocos laterais.
* Área de suporte ao estudante.

### 3. Personalizar o Comportamento

Exemplo de instrução para o Gemini:

> Você é um tutor virtual da disciplina. Responda de forma clara, objetiva e didática. Quando possível, apresente exemplos práticos e incentive o estudante a continuar aprendendo.

### 4. Fluxo de Funcionamento

**Entrada**

* Perguntas dos alunos.
* Solicitação de explicações.
* Pedidos de revisão de conteúdo.

**Processamento**

* Análise da pergunta pelo Gemini.
* Consulta ao contexto disponibilizado pelo Moodle.

**Saída**

* Respostas automáticas.
* Sugestões de estudo.
* Explicações personalizadas.
* Recomendações de materiais.

---

## 🧪 Testes e Validação

1. Crie um curso piloto.

2. Habilite o Gemini apenas para essa disciplina.

3. Teste:

   * Geração de resumos.
   * Criação de quizzes.
   * Feedback automático.
   * Interações do chatbot.

4. Solicite avaliações dos alunos e docentes.

5. Ajuste prompts e permissões conforme necessário.

---

## 🔌 Exemplo de Chamada da API Gemini

Exemplo básico em PHP:

```php
$apiKey = "SUA_API_KEY";

$url = "https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=".$apiKey;

$data = [
    "contents" => [
        [
            "parts" => [
                [
                    "text" => "Explique o conceito de portas lógicas AND e OR."
                ]
            ]
        ]
    ]
];

$options = [
    "http" => [
        "header"  => "Content-Type: application/json",
        "method"  => "POST",
        "content" => json_encode($data)
    ]
];

$context = stream_context_create($options);
$result = file_get_contents($url, false, $context);

echo $result;
```

---

## ⚠️ Pontos de Atenção

### Privacidade

* Informar os alunos sobre o uso da IA.
* Minimizar o envio de dados pessoais para a API.

### Custos

* Utilizar a camada gratuita durante o desenvolvimento.
* Monitorar o consumo quando houver expansão do uso.

### Segurança

* Nunca expor a chave da API no código-fonte público.
* Armazenar a chave em variáveis de ambiente ou configurações protegidas.

### Ética

* Manter transparência sobre recomendações geradas pela IA.
* Validar respostas críticas produzidas automaticamente.

---

## 📊 Benefícios Esperados

* Atendimento aos alunos 24 horas por dia.
* Redução do tempo de resposta às dúvidas.
* Maior engajamento nas disciplinas.
* Apoio à personalização da aprendizagem.
* Auxílio aos docentes na criação de materiais e avaliações.

---

## 📚 Estudo de Caso UTFPR

Aplicado ao curso de Engenharia Eletrônica da UTFPR – Campus Toledo:

### Objetivos

* Melhorar a retenção dos estudantes.
* Oferecer suporte contínuo fora do horário de aula.
* Reduzir a sobrecarga docente em dúvidas repetitivas.

### Resultados Esperados

* Maior participação dos alunos.
* Melhor desempenho acadêmico.
* Aumento da autonomia no processo de aprendizagem.

---

## ✅ Conclusão

A integração do Google Gemini ao Moodle oferece uma solução moderna, acessível e de baixo custo para implementação de Inteligência Artificial na Educação a Distância. Utilizando a API do Gemini, instituições podem disponibilizar tutoria inteligente, geração de conteúdo, feedback automático e chatbots educacionais, melhorando a experiência dos estudantes e ampliando a eficiência do trabalho docente.
