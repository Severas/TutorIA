# 📘 Tutorial de Integração do Copilot (IA) no Moodle

Este guia explica como configurar a API de Inteligência Artificial (Copilot) no Moodle para oferecer tutoria inteligente, feedback automático e recomendações personalizadas aos estudantes.

---

## 🔧 Pré-requisitos

- **Versão do Moodle**: 4.5 ou superior (recomendado Moodle 5.0+).
- **Acesso administrativo** ao Moodle.
- **Chave de API** do serviço de IA (Copilot via Microsoft 365 ou outro provedor compatível).
- **Servidor Moodle** com acesso à internet para chamadas externas de API.

---

## 📥 Instalação do Plugin Copilot

1. Baixe o plugin oficial: [moodle-local_copilot](https://github.com/microsoft/moodle-local_copilot)  
2. Acesse o Moodle como administrador.
3. Vá em:  
   **Site administration > Plugins > Install plugin**.
4. Carregue o arquivo `.zip` do plugin e finalize a instalação.
5. Após instalado, o Moodle reconhecerá o Copilot como um **AI provider**.

---

## ⚙️ Configuração da API

1. No painel administrativo, vá até:  
   **Site administration > General > AI**.
2. Clique em **AI providers** e selecione **Copilot**.
3. Insira sua **chave de API** fornecida pelo serviço Copilot.
4. Configure permissões:
   - **Docentes** → podem gerar resumos, criar quizzes, acompanhar desempenho.
   - **Estudantes** → podem pedir explicações, resumos de textos e recomendações de conteúdo.

---

## 🚀 Habilitar Funcionalidades

No menu **AI placements**, escolha onde o Copilot aparecerá:

- **Editor de texto** → para resumos e explicações automáticas.
- **Atividades** → feedback imediato em tarefas e fóruns.
- **Painel do professor** → relatórios de desempenho e monitoramento em tempo real.

Defina as ações disponíveis:
- Gerar texto explicativo.
- Criar quizzes automáticos.
- Recomendar materiais extras.
- Responder dúvidas frequentes.

---

## 💬 Criando um Chatbot de Auxílio aos Usuários

Com a extensão instalada, é possível configurar o Copilot como **chatbot educacional** dentro do Moodle:

1. **Ativar o Copilot como tutor inteligente**  
   - Habilite o Copilot em fóruns, atividades e no painel do curso.  
   - Os alunos poderão interagir diretamente com o assistente.

2. **Configurar AI placements para chatbot**  
   - **Fóruns** → respostas automáticas a dúvidas comuns.  
   - **Editor de texto** → resumos e explicações de conceitos.  
   - **Painel do curso** → chatbot aparece como “assistente virtual” para guiar o estudante.

3. **Personalização do chatbot**  
   - Defina se o foco será **pedagógico** (explicações, quizzes, feedback) ou **administrativo** (orientações sobre prazos, uso da plataforma).  
   - Configure permissões para que alunos interajam livremente e docentes recebam relatórios.

4. **Fluxo de funcionamento**  
   - **Entrada**: perguntas ou interações dos alunos.  
   - **Processamento**: análise da IA (Copilot) com base em dados do Moodle.  
   - **Saída**: respostas automáticas, recomendações de conteúdo, feedback imediato.

5. **Benefícios do chatbot**  
   - Responde dúvidas em tempo real.  
   - Reduz tempo de resposta docente.  
   - Aumenta engajamento e autonomia dos alunos.  
   - Libera professores para casos complexos e mentoria individual.

---

## 🧪 Testes e Validação

1. Crie um **curso piloto** e habilite o Copilot apenas nessa disciplina.
2. Teste:
   - Feedback automático em fóruns e tarefas.
   - Recomendações de conteúdo personalizadas.
   - Monitoramento em tempo real via Moodle Analytics.
3. Colete feedback dos alunos e professores.
4. Ajuste as configurações conforme os resultados.

---

## ⚠️ Pontos de Atenção

- **Privacidade**: configure coleta mínima de dados e informe os alunos sobre uso da IA.
- **Infraestrutura**: verifique se o servidor suporta chamadas externas sem lentidão.
- **Ética**: mantenha transparência sobre como a IA gera recomendações e evite vieses.
- **Consentimento**: obtenha autorização dos alunos (TCLE) para uso de dados.

---

## 📊 Benefícios Esperados

- Redução da evasão em disciplinas complexas (~30% → ~15–20%).
- Aumento do desempenho médio (6,5 → 7,5–8,0).
- Engajamento mais consistente.
- Respostas a dúvidas em minutos, liberando o professor para casos complexos.

---

## 📚 Estudo de Caso UTFPR

Aplicado no curso de Engenharia Eletrônica da UTFPR – Campus Toledo:

- **Resultados esperados**: maior retenção, melhor desempenho e engajamento contínuo.
- **Aprendizado**: IA libera docentes para atividades de maior valor agregado, como mentoria individual.

---

## ✅ Conclusão

A integração do Copilot no Moodle representa um avanço estratégico para a Educação a Distância, oferecendo suporte adaptativo, inclusivo e eficaz. Além de tutoria inteligente, é possível configurar o Copilot como **chatbot educacional**, ampliando o suporte aos alunos e otimizando o trabalho docente.
