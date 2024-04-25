# Atividade da Disciplina de Segurança de Computadores

## Introdução

Essa atividade consiste em responder questões e realizar desenhos relacionados aos conceitos abordados na disciplina de Segurança de Computadores.

### Questões

1. **O que é a arquitetura de segurança OSI?**
   - A arquitetura de segurança OSI define os requisitos e técnicas para garantir a segurança em redes de computadores de uma organização. Ela serve como um guia para organizar a implementação de medidas de segurança. Esta arquitetura se concentra em três aspectos principais: ataques à segurança, mecanismos de segurança e serviços de segurança.

2. **Qual é a diferença entre ameaças à segurança passivas e ativas?**
   - As ameaças à segurança passivas são caracterizadas pelo monitoramento ou bisbilhotagem das transmissões de dados, enquanto as ativas envolvem a modificação do fluxo de dados ou a criação de fluxos falsos.

3. **Liste e defina resumidamente as categorias de ataques passivos e ativos à segurança.**
   - **Ataques Passivos:** Vazamento de Conteúdo de Mensagem, Análise de Tráfego.
   - **Ataques Ativos:** Disfarce, Repasse, Modificação de Mensagens, Negação de Serviço.

4. **Liste e defina resumidamente as categorias dos serviços de segurança.**
   - Autenticação, Controle de Acesso, Confidencialidade dos Dados, Integridade dos Dados, Irretratabilidade, Serviço de Disponibilidade.

5. **Liste e defina resumidamente as categorias dos mecanismos de segurança.**
   - Mecanismos de segurança específicos: Codificação, Assinatura digital, Controle de acesso, Integridade de dados, Troca de autenticação, Preenchimento de tráfego, Controle de roteamento, Notarização.
   - Mecanismos de segurança difusos: Funcionalidade confiada, Rótulo de segurança, Detecção de evento, Trilha de auditoria de segurança, Recuperação de segurança.

6. **Considere um caixa eletrônico (ATM). Dê exemplos de requisitos de confidencialidade, integridade e disponibilidade associados com esse sistema.**
   - **Confidencialidade:** Garantir que as informações dos usuários sejam mantidas em sigilo.
   - **Integridade:** Assegurar que as transações não sejam alteradas.
   - **Disponibilidade:** Garantir que o sistema esteja sempre disponível.

7. **Desenhe matrizes mostrando o relacionamento entre serviços de segurança e ataques, e entre mecanismos de segurança e ataques.**

### Matriz de Relacionamento entre Serviços de Segurança e Ataques

|          | Vazamento de Conteúdo | Análise de Tráfego | Disfarce | Repasse | Modificação de Mensagem | Negação de Serviço |
|----------|------------------------|---------------------|----------|---------|-------------------------|---------------------|
| Autenticação | X | | | | | |
| Controle de Acesso | X | | | | | |
| Conf. de Dados | X | X | | | | |
| Int. de Dados | | | X | X | X | X |
| Irretratabilidade | | | | | | X |
| Serviço de Disponibilidade | | | | | | X |

### Matriz de Relacionamento entre Mecanismos de Segurança e Ataques

|          | Vazamento de Conteúdo | Análise de Tráfego | Disfarce | Repasse | Modificação de Mensagem | Negação de Serviço |
|----------|------------------------|---------------------|----------|---------|-------------------------|---------------------|
| Codificação | X | X | X | X | X | |
| Assinatura Digital | | | | | | X |
| Controle de Acesso | X | | | | | X |
| Integridade de Dados | | | | | X | X |
| Troca de Autenticação | X | | X | | | |
| Preenchimento de Tráfego | | X | | | | |
| Contr. de Roteamento | X | | | | | X |
| Notalização | | | X | | | |
