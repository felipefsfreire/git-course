# Bem-vindo!

Este repositório foi criado para promover boas práticas no desenvolvimento colaborativo, utilizando o **Git** como sistema de controle de versão e o **GitHub** como plataforma de colaboração e hospedagem de código. Aqui você encontrará informações e exemplos para estruturar projetos de forma organizada, segura e eficiente.  

## Por que usar Git e GitHub?  

### **Benefícios do Versionamento de Código**  
- **Organização e Controle**: Gerencie alterações no código com histórico detalhado de contribuições.  
- **Colaboração**: Trabalhe em equipe, criando ramificações para diferentes funcionalidades e integrando-as facilmente.  
- **Segurança**: Mantenha backups completos com um fluxo de trabalho distribuído.  

### **Git vs GitHub**  
- **Git**: Um sistema distribuído de controle de versão (DVCS) para rastrear alterações no código.  
- **GitHub**: Uma plataforma que utiliza Git para facilitar a colaboração entre desenvolvedores.  

## Regras de Colaboração  

- **Use mensagens de commit claras e descritivas.**  
- **Sempre trabalhe em uma branch separada.**  
- **Revise e teste seu código antes de enviar.**  
- **Resolva conflitos com cuidado e mantenha uma comunicação aberta com a equipe.**  

## Recursos Adicionais  

- [Documentação Oficial do Git](https://git-scm.com/doc)  
- [Guia Prático do GitHub](https://docs.github.com/)

# **Princípios de Desenvolvimento Colaborativo com Git e GitHub**  

### **O que é Versionamento de Código?**  
- **Definição**: Versionamento é o processo de gerenciar alterações em um projeto ao longo do tempo, permitindo que diferentes colaboradores trabalhem simultaneamente sem interferir no trabalho uns dos outros.  
- **Vantagens**:  
  - Criação de **ramificações (branches)** para funcionalidades ou correções independentes.  
  - Registro de histórico: Autor, data e descrição de alterações.  
  - Organização, controle e segurança no desenvolvimento.  

---

### **Tipos de Sistemas de Controle de Versão (VCS)**  

| Tipo                | Características                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------|
| **VCS Centralizado (CVCS)** | Único repositório central; colaboradores trabalham com cópias locais.                                                |
| **VCS Distribuído (DVCS)**   | Cada colaborador possui um repositório completo, permitindo trabalho offline e maior segurança.                        |  

**Exemplo Visual**:  

```  
CVCS:
Repositório Central <--> Cópia Local  

DVCS:  
Repositório Central <--> Cópia Completa (com histórico)  
```  

---

### **O que é Git?**  
- Sistema **Distribuído de Controle de Versão (DVCS)**.  
- **Gratuito** e **Open Source**.  
- Oferece suporte eficiente para ramificações (**branching**) e fusões (**merging**).  
- [Acesse a documentação oficial do Git](https://git-scm.com/doc).  

---

### **Fluxo Básico no Git**  

| Comando       | Descrição                                                                                  |
|---------------|------------------------------------------------------------------------------------------|
| `git clone`   | Clona um repositório existente para o local.                                             |
| `git commit`  | Salva alterações no repositório local.                                                   |
| `git pull`    | Atualiza o repositório local com alterações remotas.                                     |
| `git push`    | Envia alterações locais para o repositório remoto.                                       |  

---

### **O que é GitHub?**  
- **Plataforma de hospedagem de código** que utiliza o Git para controle de versão.  
- Facilita a colaboração entre desenvolvedores.  

**Git ≠ GitHub**  
- **Git**: Ferramenta de controle de versão.  
- **GitHub**: Plataforma para colaboração e hospedagem.  

---

## **Primeiros Passos com Git e GitHub**  

### **Criando e Clonando Repositórios**  
1. Criar repositório local e vinculá-lo ao GitHub:  
   ```bash
   mkdir nome-pasta
   cd nome-pasta
   git init
   git remote add origin URL-repositório-GitHub
   ```  

2. Clonar um repositório existente:  
   ```bash
   git clone URL-repositório-GitHub
   git clone URL-repositório-GitHub nome-nova-pasta
   ```  

---

### **Salvando Alterações**  

**Cenário Prático**:  
1. Você criou um arquivo `index.html` e deseja salvar o progresso no Git:  

   ```bash
   git status                 # Verificar status
   git add index.html         # Adicionar à área de preparação
   git commit -m "Adiciona arquivo index.html"   # Salvar alterações no repositório
   git push                   # Enviar alterações para o GitHub
   ```  

---

### **Desfazendo Alterações**  

| Situação                          | Comando                                                       |
|-----------------------------------|--------------------------------------------------------------|
| Restaurar última versão do arquivo| `git restore nome-arquivo`                                   |
| Alterar mensagem do último commit | `git commit --amend -m "nova mensagem"`                      |
| Reverter um commit                | `git reset --soft hash-commit` ou `git reset --hard hash-commit` |  

---

### **Trabalhando com Branches**  

**Cenário Prático**: Criando uma nova funcionalidade em uma branch.  
1. Criar e alternar para uma branch:  
   ```bash
   git checkout -b nova-funcionalidade  
   ```  
2. Fazer alterações e salvar:  
   ```bash
   git add .
   git commit -m "Adiciona nova funcionalidade"  
   ```  
3. Mesclar a branch com a principal:  
   ```bash
   git checkout main
   git merge nova-funcionalidade
   ```  
4. Resolver conflitos (se existirem):  
   - Editar os arquivos manualmente.  
   - Marcar resolução com `git add arquivo`.  
   - Finalizar com `git commit`.  

---

### **Exercícios Práticos**  

1. **Configuração Inicial**  
   - Crie um repositório local chamado `meu-projeto`.  
   - Adicione o arquivo `README.md` com uma descrição do projeto.  
   - Envie para um repositório remoto no GitHub.  

2. **Fluxo de Trabalho em Equipe**  
   - Clone o repositório [Exemplo Colaborativo](https://github.com/user/exemplo).  
   - Crie uma branch `minha-contribuicao` e adicione uma nova funcionalidade.  
   - Mescle sua branch com a principal e envie as alterações.  

3. **Resolução de Conflitos**  
   - Simule um conflito alterando a mesma linha em duas branches diferentes.  
   - Resolva o conflito e finalize o merge.  

---

### **Material de Apoio**  
- [Documentação Git](https://git-scm.com/doc)  
- Diagramas de Fluxo:  

```  
Fluxo de Trabalho Básico:
Git Add --> Git Commit --> Git Push  
```  

Contribuir de forma eficiente com Git e GitHub é um passo essencial para o sucesso de qualquer equipe de desenvolvimento. Colabore, aprenda e evolua!  

---  

**Observação**: Sinta-se à vontade para abrir issues ou pull requests para melhorar este repositório e compartilhar novas ideias.
