**Nome completo**: Luiz Fellipe de Almeida Rodrigues Barbosa

### Questões e Respostas

## 1. **O que é a arquitetura de segurança OSI?**
A arquitetura de segurança OSI define os requisitos e técnicas para garantir a segurança em redes de computadores de uma organização. Ela serve como um guia para organizar a implementação de medidas de segurança. Esta arquitetura se concentra em três aspectos principais: ataques à segurança, mecanismos de segurança e serviços de segurança. Podendo serem resumidos da seguinte forma:
- Ataque à segurança: refere-se a qualquer ação que comprometa a segurança da informação de uma organização.
- Mecanismo de segurança: são processos ou dispositivos projetados para detectar, prevenir ou recuperar-se de - ataques à segurança.
- Serviço de segurança: engloba as funções oferecidas pelos mecanismos de segurança para proteger a rede e os   dados contra ameaças. 
Essa abordagem ajuda a compreender melhor os riscos de segurança e a implementar medidas adequadas para proteger as redes e os sistemas de uma organização.

## 2. **Qual é a diferença entre ameaças à segurança passivas e ativas?**
As ameaças à segurança passivas são caracterizadas pelo monitoramento ou bisbilhotagem das transmissões de dados, com o objetivo de obter informações sem modificar o fluxo de dados. Exemplos incluem vazamento de conteúdo de mensagem e análise de tráfego. Por outro lado, as ameaças à segurança ativas envolvem a modificação do fluxo de dados ou a criação de fluxos falsos, como disfarce, repasse, modificação de mensagens e negação de serviço. De modo geral, as ameaças passivas visam obter informações sem alterar os dados, enquanto as ameaças ativas envolvem a modificação ou interrupção do fluxo de dados.

## 3. **Liste e defina resumidamente as categorias de ataques passivos e ativos à segurança.**

- **Ataques Passivos:**
    - Vazamento de Conteúdo de Mensagem: Bisbilhotar transmissões para obter informações sensíveis ou confidenciais.
    - Análise de Tráfego: Observar padrões de comunicação, mesmo que o conteúdo esteja encriptado, para deduzir informações sobre a natureza da comunicação.
- **Ataques Ativos:**
    - Disfarce: Fingir ser outra entidade para obter acesso não autorizado.
    - Repasse: Capturar e retransmitir dados para produzir um efeito não autorizado.
    - Modificação de Mensagens: Alterar partes de uma mensagem legítima para alcançar um resultado não autorizado.
    - Negação de Serviço: Inibir ou impedir o uso normal de instalações de comunicação, seja direcionado ataques a um alvo específico ou perturbando toda uma rede.

## 4. **Liste e defina resumidamente as categorias dos serviços de segurança.**

- Autenticação: Garante a certeza de que a entidade comunicante é realmente quem afirma ser. Isso inclui autenticação da entidade pareada, que verifica a identidade das entidades em uma conexão, e autenticação da origem de dados, que autentica a origem de uma unidade de dados.
- Controle de Acesso: Previne o uso não autorizado de recursos, controlando quem pode acessá-los, sob que condições e o que é permitido para quem acessa.
- Confidencialidade dos Dados: Protege os dados contra divulgação não autorizada. Isso pode incluir a confidencialidade da conexão, confidencialidade sem conexão, confidencialidade com campo seletivo e confidencialidade do fluxo de tráfego.
- Integridade dos Dados: Garante que os dados recebidos sejam exatamente conforme enviados por uma entidade autorizada, sem modificações, inserções, exclusões ou repasses. Isso pode envolver integridade da conexão com recuperação, integridade da conexão sem recuperação, integridade da conexão com campo seletivo, integridade sem conexão e integridade sem conexão com campo seletivo.
- Irretratabilidade: Impede que o emissor ou o receptor neguem uma mensagem transmitida, fornecendo prova de que a mensagem foi enviada pela parte especificada (irretratabilidade de origem) ou prova de que a mensagem foi recebida pela parte especificada (irretratabilidade de destino).
- Serviço de Disponibilidade: Garante que um sistema ou recurso do sistema seja acessível e utilizável sob demanda por uma entidade autorizada, de acordo com as especificações de desempenho. Isso inclui proteção contra ataques de negação de serviço e depende do gerenciamento adequado dos recursos do sistema.


## 5. **Liste e defina resumidamente as categorias dos mecanismos de segurança.**

- **Mecanismos de segurança específicos:**
    - Codificação: Utilização de algoritmos matemáticos para transformar os dados em um formato não prontamente inteligível, geralmente com o uso de chaves de encriptação.
    - Assinatura digital: Dados anexados a uma unidade de dados que permitem que o destinatário prove sua origem e integridade e protege contra falsificação.
    - Controle de acesso: Conjunto de mecanismos que impõem direitos de acesso aos recursos.
    - Integridade de dados: Conjunto de mecanismos usados para garantir a integridade de uma unidade de dados ou fluxo de unidades de dados.
    - Troca de autenticação: Mecanismo para garantir a identidade de uma entidade por meio da troca de informações.
    - Preenchimento de tráfego: Inserção de bits nas lacunas de um fluxo de dados para frustrar análises de tráfego.
    - Controle de roteamento: Permite a seleção de rotas seguras para determinados dados e mudanças de roteamento.
    - Notarização: Uso de um terceiro confiável para garantir certas propriedades de uma troca de dados.
- **Mecanismos de segurança difusos:**
    -  Funcionalidade confiada: Aquilo que é percebido como correto de acordo com critérios estabelecidos por uma política de segurança.
    - Rótulo de segurança: Marcação vinculada a um recurso que nomeia ou designa os atributos de segurança desse recurso.
    - Detecção de evento: Detecção de eventos relevantes à segurança.
    - Trilha de auditoria de segurança: Dados coletados e potencialmente utilizados para facilitar uma auditoria de segurança.
    - Recuperação de segurança: Lida com solicitações de mecanismos de tratamento e gerenciamento de eventos e toma medidas de recuperação.


## 6. **Considere um caixa eletrônico (ATM). Dê exemplos de requisitos de confidencialidade, integridade e disponibilidade associados com esse sistema.**

**Confidencialidade:**
- Requisito: Garantir que as informações pessoais dos usuários, como números de conta e senhas, sejam mantidas em sigilo e não sejam acessíveis a pessoas não autorizadas.
- Importância: Muito alta. A confidencialidade é fundamental para proteger os dados sensíveis dos clientes contra acesso não autorizado, prevenindo assim o roubo de identidade e a fraude financeira.
**Integridade:**
- Requisito: Assegurar que as transações realizadas pelos usuários não sejam alteradas durante o processo de transferência de dados entre o ATM e o banco.
- Importância: Alta. A integridade garante que as transações sejam processadas conforme a intenção do usuário e que não sejam adulteradas ou corrompidas no meio do caminho, evitando assim a perda de fundos e problemas de contabilidade.
**Disponibilidade:**
- Requisito: Garantir que o sistema ATM esteja sempre disponível para os usuários realizarem transações, sem interrupções significativas ou tempos de inatividade prolongados.
- Importância: Muito alta. A disponibilidade é crucial para garantir que os clientes possam acessar seus fundos a qualquer momento, especialmente em situações de emergência. Qualquer interrupção no serviço pode causar inconvenientes aos usuários e afetar a reputação do banco.

Esses requisitos são fundamentais para garantir a segurança e o bom funcionamento de um sistema ATM, e sua importância é refletida na necessidade de implementar medidas robustas de segurança e manutenção para atender a esses requisitos.

 

## 7. **Desenhe matrizes mostrando o relacionamento entre serviços de segurança e ataques, e entre mecanismos de segurança e ataques.**

**Matriz de Relacionamento entre Serviços de Segurança e Ataques**

Serviços = linhas; Ataques = colunas
||Vazamento de conteúdo de mensagem|Análise de tráfego|Disfarce|Repasse|Modificação de mensagens|
| :- | :-: | :-: | :-: | :-: | :-: |
|Autenticação de entidade paralela|S||S|S|S|
|Autenticação da origem de dados|S||S|S|S|
|Controle de acesso|S||S|S||
|Confidencialidade|S||S|S|S|
|Confidencialidade de fluxo de tráfego|S|S|S|S|S|
|Integridade de dados|||||S|
|Responsabilização|||S|||
|Disponibilidade||||||

&nbsp;

**Matriz de Relacionamento entre Mecanismos de Segurança e Ataques**

Mecanismos = linhas; Ataques = colunas
||Vazamento de conteúdo de mensagem|Análise de tráfego|Disfarce|Repasse|Modificação de mensagens|
| :- | :-: | :-: | :-: | :-: | :-: |
|Codificação|S|S|S|S|S|
|Assinatura digital|S|S|S|S|S|
|Controle de acesso|S||S|S|S|
|Integridade de dados|||||S|
|Troca de autenticação|S|S|S|S||
|Preenchimento de tráfego||S||||
|Controle de roteamento|S|||S||
|Notarização|S||S|S|S|

&nbsp;

Livro-texto da disciplina:

STALLINGS, William. Criptografia e segurança de redes. Princípios e práticas, Ed. 6. 2014.