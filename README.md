# Desafio Técnico — Estágio Full Stack | Vylcor
 
A ideia desse desafio é ver como você pensa, como organiza um projeto do zero e como comunica suas decisões. Não existe uma única resposta certa.
 
> **Prazo de entrega:** 10 dias corridos a partir do recebimento deste link.
 
---
 
## O problema
 
A **Barbearia Vylbeard** ainda controla os agendamentos em um caderno na recepção. Isso gera três dores diárias:
 
1. Dois clientes marcados com o mesmo barbeiro no mesmo horário.
2. Ninguém sabe quantos atendimentos estão marcados para o dia até abrir a agenda.
3. O barbeiro não tem visibilidade da própria agenda fora da loja.
Sua missão é construir um **sistema web de agendamento** que resolva essas dores.
 
O sistema é de **uso interno da barbearia**, quem opera é a recepção e os barbeiros, não o cliente final.
 
---
 
## Requisitos obrigatórios
 
Esses são os itens que precisam existir para a entrega ser considerada completa.
 
### 1. Serviços
- Cadastrar, listar, editar e remover serviços.
- Cada serviço tem: **nome**, **duração em minutos** e **preço**.
- Exemplos: Corte (30 min, R$ 45), Barba (20 min, R$ 30), Corte + Barba (50 min, R$ 70).
### 2. Barbeiros
- Cadastrar, listar, editar e remover barbeiros.
- Cada barbeiro tem no mínimo: **nome** e **telefone**.
### 3. Agendamentos
- Criar, listar, editar e cancelar agendamentos.
- Cada agendamento tem: **nome do cliente**, **telefone do cliente**, **barbeiro**, **serviço**, **data e hora de início** e **status**.
- O horário de término é calculado automaticamente a partir da duração do serviço.
- Status possíveis: `agendado`, `concluído`, `cancelado`.
### 4. Regras de negócio (a parte que mais nos interessa)
 
Estas validações precisam ser garantidas pelo **back-end**, não apenas pela tela:
 
- **Sem conflito de horário:** um mesmo barbeiro não pode ter dois agendamentos que se sobreponham no tempo. Atenção: considere a duração, não só o horário de início. Um corte às 10h00 (30 min) impede um agendamento às 10h15.
- **Sem agendamento no passado:** não é possível marcar para uma data/hora que já passou.
- **Horário de funcionamento:** a barbearia atende de **segunda a sábado, das 09h00 às 19h00**. O agendamento precisa começar **e terminar** dentro dessa janela.
- Agendamentos cancelados liberam o horário para novos agendamentos.
### 5. Agenda do dia
- Uma tela que mostre os agendamentos de uma data específica.
- Deve ser possível **filtrar por barbeiro**.
- Ordenados por horário.
---
 
## 🛠️ Requisitos técnicos
 
- **A stack é livre.** Use as tecnologias em que você se sente mais confortável ou que quer mostrar.
- O projeto precisa ter **front-end e back-end** (podem estar no mesmo repositório e até no mesmo framework, como Next.js ou Laravel com Blade/Inertia).
- Persistência em **banco de dados** (relacional ou não). Não vale guardar em memória ou em array.
- O código precisa rodar na nossa máquina seguindo o seu README. Se não rodar, não conseguimos avaliar.
- Versionamento com **Git**, com commits ao longo do desenvolvimento (evite um único commit "primeiro commit" com tudo dentro).
---
 
## Diferenciais
 
**Nada aqui é obrigatório.** Preferimos os requisitos obrigatórios bem feitos do que todos os diferenciais pela metade. Escolha um ou dois que façam sentido pra você:
 
- Testes automatizados (principalmente da regra de conflito de horário)
- Autenticação e login
- Docker / docker-compose para subir o projeto
- Deploy em ambiente público (Vercel, Railway, Render, Fly.io...)
- Interface responsiva (a recepção usa tablet)
- Documentação de API (Swagger / Scalar / Insomnia collection)
- Seeds com dados de exemplo
- Dashboard com total de atendimentos e faturamento previsto do dia
- Validação e tratamento de erros com mensagens claras ao usuário
---

 
## Como entregar
 
1. Crie um repositório **público** na sua conta do GitHub.
2. Desenvolva o projeto lá.
3. Envie o link do repositório para **contato@vylcor.com.br** com o assunto **"Desafio Estágio Full Stack — [Seu Nome]"**.
### O README do seu projeto deve conter:
 
- Quais tecnologias você usou e **por quê**
- Como rodar o projeto localmente (passo a passo, incluindo variáveis de ambiente e banco)
- O que ficou faltando ou incompleto (ser honesto aqui conta a favor, não contra)
 
---
 
## Sobre o uso de IA
 
Usar ChatGPT, Claude, Copilot ou similar é **permitido e esperado**, faz parte do dia a dia aqui.
 
O único combinado é: **você precisa entender e saber explicar cada linha do que entregou.** Na etapa seguinte teremos uma conversa técnica de cerca de 30 minutos sobre o seu código, onde vamos pedir para você explicar decisões e, caso necessário, implementar uma pequena mudança ao vivo.
 
Código gerado por IA que o candidato não sabe explicar é o que mais elimina gente nessa etapa. Use como ferramenta, não como atalho.
 
---
 
## Dúvidas
 
Ficou algo confuso no enunciado? Entre em contato conosco via email contato@vylcor.com.
 
Boa sorte, e divirta-se construindo. 🚀
 
**Equipe Vylcor**
