# Projeto ERP — Lavanderia ST Bárbara

Projeto Integrador — Modelagem de Dados

Este projeto tem como objetivo transformar os processos reais de uma microempresa de lavanderia em uma estrutura organizada de informações, passando pela identificação de problemas, requisitos e regras de negócio até o Modelo Conceitual de Dados e o DER.

---

## 01. Identificação da equipe

**Empresa analisada:** Lavanderia ST Bárbara

**Equipe:** *Preencher com os nomes dos integrantes.*

---

## 02. Caracterização da empresa

### Nome
**Lavanderia ST Bárbara**

### Segmento
Lavanderia, com serviços de lavagem geral e atendimento a diferentes nichos.

### Serviços oferecidos
- Lavagem de peças;
- Secagem;
- Passagem;
- Restauração em casos específicos.

### Principais clientes
A lavanderia atende pessoas e empresas que procuram serviços de lavagem mais especializados.

### Principais setores
- Atendimento;
- Inventário;
- Lavagem;
- Secagem;
- Passagem;
- Restauração, quando necessária.

### Funcionamento atual
O cliente chega ao atendimento e realiza um pedido. O atendente registra em uma comanda o item ou peça, o serviço que será realizado e um prazo de entrega.

Após o registro, a peça passa pelos processos correspondentes ao serviço contratado. Quando fica pronta, o cliente é avisado para realizar a retirada.

Em casos específicos, pode ser realizada a entrega da peça ao cliente.

Atualmente, grande parte do processo depende de controles manuais e de conhecimentos que estão concentrados na experiência da responsável pela empresa.

### Informações importantes para o negócio
A precificação é um dos pontos importantes do funcionamento da lavanderia.

Cada item possui um valor associado e, posteriormente, é acrescentado o valor do serviço. A precificação também considera características como tipos de tecidos, malhas, costuras, técnicas e estilos.

Exemplos levantados:
- Sapato: R$ 55,00 + R$ 30,00 de lavagem = R$ 85,00;
- Edredom: R$ 140,00 + R$ 100,00 de lavagem = R$ 240,00.

Essas informações atualmente estão principalmente na memória da responsável pela empresa, o que dificulta a previsibilidade de custos e prazos.

Também são importantes informações como:
- Nome do cliente;
- Número do pedido;
- Telefone para contato;
- Segundo telefone, quando necessário;
- Endereço, em casos específicos;
- Item ou peça;
- Serviço solicitado;
- Prazo de entrega;
- Preço e custo;
- Necessidade de entrega.

---

## 03. Justificativa da escolha

A Lavanderia ST Bárbara foi escolhida porque possui processos que podem ser analisados e apresenta uma necessidade de organização das informações.

Um dos principais pontos identificados é a utilização de comandas genéricas para registrar os pedidos. Embora a responsável conheça os custos e critérios utilizados na precificação, muitas dessas informações não estão formalizadas.

Essa situação dificulta principalmente:
- A compreensão de como o preço foi determinado;
- A definição e previsibilidade de prazos;
- O acompanhamento do pedido durante o processo interno;
- A criação de um cadastro estruturado;
- A futura sistematização dos processos da empresa.

A ausência de um sistema de cadastro de pedidos também representa uma oportunidade para aplicação de uma solução ERP adequada à realidade da empresa.

---

## 04. Problemas identificados

| Problema | Consequência |
|---|---|
| Comandas genéricas | Dificuldade para compreender detalhadamente o pedido |
| Informações de precificação concentradas na memória | Dificuldade de rastrear como o preço foi definido e de prever custos |
| Controles predominantemente manuais | Dificuldade de organização e acompanhamento |
| Ausência de cadastro estruturado de clientes | Identificação baseada principalmente em anotações |
| Ausência de diferenciação clara das etapas internas | Dificuldade para saber em qual fase um pedido se encontra |
| Informações intrínsecas ao processo não documentadas | Dificuldade para uma pessoa externa compreender o processo |
| Ausência de sistema de cadastro de pedidos | Dificuldade de sistematização e acompanhamento |

Apesar dos problemas de organização, a responsável informou que erros e perdas de pedidos são raros. O principal problema identificado está na falta de formalização e rastreabilidade das informações.

---

## 05. Processos de negócio

O processo principal identificado pode ser representado da seguinte forma:

```text
Cliente
   ↓
Pedido
   ↓
Serviço
   ↓
Processo interno
   ↓
Estoque
   ↓
Pagamento
```

Quando há necessidade de entrega:

```text
Cliente
   ↓
Pedido
   ↓
Serviço
   ↓
Processo interno
   ↓
Estoque
   ↓
Entrega
   ↓
Pagamento
```

### Participantes
- Cliente;
- Atendente;
- Responsáveis pelos processos internos.

### Início do processo
O processo é iniciado pelo cliente ao solicitar um serviço.

### Informações geradas
- Nome do cliente;
- Número do pedido;
- Item;
- Serviço;
- Prazo;
- Preço/custo;
- Necessidade de entrega.

### Resultado
O resultado esperado é a disponibilização da peça ao cliente e a realização do pagamento.

---

## 06. Requisitos funcionais

Os requisitos funcionais representam as funções que o sistema deverá realizar.

### RF01 — Cadastrar cliente
O sistema deverá permitir o cadastro de clientes.

### RF02 — Alterar cadastro do cliente
O sistema deverá permitir a alteração dos dados cadastrados de um cliente.

### RF03 — Registrar pedido
O sistema deverá permitir o registro de pedidos.

### RF04 — Finalizar pedido
O sistema deverá permitir a finalização de pedidos.

### RF05 — Registrar pagamento
O sistema deverá permitir o registro do pagamento de um pedido.

### RF06 — Controlar inventário
O sistema deverá permitir o controle do inventário.

### RF07 — Gerenciar prazos
O sistema deverá permitir o gerenciamento dos prazos dos pedidos.

### RF08 — Gerenciar processos internos
O sistema deverá permitir o gerenciamento das etapas internas pelas quais um item passa.

### RF09 — Rastrear pedidos
O sistema deverá permitir acompanhar os pedidos durante o processo interno.

### RF10 — Selecionar etapa do processo
O sistema deverá permitir selecionar a etapa atual de um item.

### RF11 — Alterar etapa do processo
O sistema deverá permitir alterar a etapa de um item durante o processo.

### RF12 — Cadastrar itens e serviços
O sistema deverá permitir cadastrar novos itens e seus respectivos serviços.

### RF13 — Exclusão de dados
O sistema deverá permitir a exclusão de dados de pedidos de acordo com as regras definidas pela empresa.

---

## 07. Requisitos não funcionais

Os requisitos não funcionais descrevem características e condições de funcionamento do sistema.

### RNF01 — Retenção dos pedidos
O sistema deverá manter registros dos pedidos por no mínimo 6 meses.

### RNF02 — Identificação dos pedidos
O sistema deverá permitir o cadastro e a finalização dos pedidos utilizando um código de barras.

> Outros requisitos não funcionais relacionados a segurança, desempenho, disponibilidade, usabilidade e controle de acesso deverão ser definidos após a análise das condições do equipamento e das necessidades da empresa.

---

## 08. Regras de negócio

As regras de negócio deverão representar as condições que precisam ser respeitadas pelo funcionamento da lavanderia e pelo sistema.

Com base no levantamento realizado, algumas regras ainda precisam ser formalizadas pela equipe.

### Regras a definir
- Critérios utilizados para determinar o preço final de cada serviço;
- Critérios utilizados para determinar o prazo de entrega;
- Condições para alteração das etapas de um pedido;
- Condições para finalização de um pedido;
- Condições para pagamento;
- Condições para entrega;
- Regras para exclusão de dados de pedidos;
- Regras específicas para serviços de restauração;
- Regras relacionadas aos diferentes tipos de tecidos, malhas e costuras.

---

## 09. Restrições e políticas organizacionais

Até o momento, o levantamento ainda não documentou completamente as restrições e políticas organizacionais.

Esta seção deverá registrar decisões da empresa que precisem ser respeitadas pelo sistema, como:
- Quem pode alterar informações de pedidos;
- Quem pode finalizar pedidos;
- Quem pode alterar etapas do processo;
- Quem pode alterar informações de clientes;
- Condições para cancelamento;
- Condições de pagamento;
- Políticas relacionadas à entrega;
- Políticas de acesso às informações.

**A equipe deverá validar essas regras com a empresa antes da versão final.**

---

## 10. Fluxogramas

Os fluxogramas devem representar os processos reais da lavanderia e manter coerência com os requisitos e regras de negócio.

### Processo principal

```text
INÍCIO
   ↓
Cliente realiza pedido
   ↓
Registrar item e serviço
   ↓
Definir prazo e preço
   ↓
Encaminhar peça para o processo interno
   ↓
Realizar serviço
   ↓
Peça pronta?
 ┌───────┴───────┐
 NÃO             SIM
 ↓                ↓
Continuar       Disponibilizar
processamento   para o cliente
                  ↓
             Precisa entregar?
              ┌────┴────┐
             SIM        NÃO
              ↓          ↓
           Entregar    Aguardar
              ↓        retirada
              └────┬─────┘
                   ↓
                Pagamento
                   ↓
                  FIM
```

> Os fluxogramas visuais finais deverão ser anexados ao repositório.

---

## 11. Entidades

As entidades devem representar informações relevantes do negócio que precisam ser armazenadas.

Com base nos processos e requisitos levantados, as principais entidades a serem analisadas são:
- **Cliente**
- **Pedido**
- **Item/Peça**
- **Serviço**
- **Etapa do processo**
- **Pagamento**
- **Entrega**

> A definição final das entidades deverá ser validada durante a modelagem conceitual, evitando transformar todo substantivo identificado em uma entidade sem justificativa.

---

## 12. Atributos

Os atributos representam as informações que precisam ser armazenadas sobre cada entidade.

### Cliente
- ID do cliente;
- Nome;
- Telefone;
- Segundo telefone;
- Endereço, quando necessário.

### Pedido
- ID do pedido;
- Data do pedido;
- Prazo de entrega;
- Preço;
- Status;
- Código de barras.

### Item/Peça
- ID do item;
- Tipo de peça;
- Características do tecido;
- Características da malha;
- Características da costura.

### Serviço
- ID do serviço;
- Nome do serviço;
- Valor do serviço;
- Descrição.

### Pagamento
- ID do pagamento;
- Valor;
- Data;
- Forma de pagamento;
- Status.

> Os atributos definitivos deverão ser definidos após a validação das entidades, regras e necessidades do negócio.

---

## 13. Relacionamentos

Os relacionamentos deverão representar as interações reais identificadas no negócio.

Possíveis relacionamentos:
- **Cliente realiza Pedido**
- **Pedido possui Item/Peça**
- **Pedido possui Serviço**
- **Item/Peça passa por Etapa**
- **Pedido possui Pagamento**
- **Pedido pode possuir Entrega**

Os relacionamentos definitivos deverão ser definidos juntamente com suas regras e cardinalidades.

---

## 14. Cardinalidades

As cardinalidades deverão ser definidas analisando os dois sentidos de cada relacionamento e utilizando as regras de negócio como justificativa.

### Exemplo a ser analisado

```text
CLIENTE (0,N) — REALIZA — PEDIDO (1,1)
```

Interpretação:
- Um cliente pode não possuir nenhum pedido ou possuir vários;
- Cada pedido pertence a um cliente.

Os demais relacionamentos deverão seguir o mesmo método de análise.

> As cardinalidades finais deverão ser confirmadas pela equipe antes da elaboração do DER.

---

## 15. Dicionário de dados conceitual

| Entidade | Atributo | Descrição | Regra/Observação |
|---|---|---|---|
| Cliente | id_cliente | Identificador do cliente | Identificação única |
| Cliente | nome | Nome do cliente | Utilizado para identificação |
| Cliente | telefone | Telefone do cliente | Utilizado para contato |
| Cliente | endereco | Endereço do cliente | Necessário em casos específicos |
| Pedido | id_pedido | Identificador do pedido | Identificação única |
| Pedido | prazo | Prazo previsto para entrega | Definido durante o atendimento |
| Pedido | preco | Valor do pedido | Depende do item e do serviço |
| Pedido | codigo_barras | Código de identificação | Relacionado ao requisito de rastreamento |
| Item | tipo | Tipo de peça/item | Ex.: sapato, edredom |
| Serviço | descricao | Serviço realizado | Ex.: lavagem |
| Pagamento | valor | Valor pago | Relacionado ao pedido |

> O dicionário deverá ser ampliado e validado conforme a equipe finalizar as entidades, atributos e regras de negócio.

---

## 16. DER

O Diagrama Entidade-Relacionamento deverá representar o resultado da análise realizada neste projeto.

O DER deverá conter:
- Entidades;
- Atributos;
- Relacionamentos;
- Cardinalidades;
- Regras de negócio relevantes;
- Atributos pertencentes aos relacionamentos, quando existirem.

### Fluxo de construção

```text
Problema real
     ↓
Processos
     ↓
Requisitos
     ↓
Regras de negócio
     ↓
Entidades
     ↓
Atributos
     ↓
Relacionamentos
     ↓
Cardinalidades
     ↓
DER
```

O DER final deverá ser anexado ao repositório.

---

## 17. Justificativas técnicas

As decisões de modelagem deverão ser justificadas com base nos processos, requisitos e regras de negócio identificados.

### Cadastro de clientes
A entidade Cliente é necessária porque o negócio precisa identificar quem realizou o pedido e manter informações de contato.

### Cadastro de pedidos
A entidade Pedido é necessária para representar a solicitação realizada pelo cliente e organizar informações como prazo, preço e acompanhamento do serviço.

### Acompanhamento das etapas
O acompanhamento das etapas é necessário porque atualmente não existe uma diferenciação clara das fases pelas quais uma peça passa durante o processo interno. A modelagem deverá permitir representar esse acompanhamento.

### Precificação
A precificação merece atenção na modelagem porque depende de características do item e do serviço realizado. Atualmente, parte relevante dessas informações está concentrada no conhecimento da responsável pela empresa.

### Cardinalidades
As cardinalidades deverão ser definidas a partir das regras de negócio, analisando os dois sentidos de cada relacionamento, e não apenas pela aparência do modelo.

---

## 18. Conclusão

A análise inicial da Lavanderia ST Bárbara mostrou que o principal desafio está na ausência de uma estrutura formal para registrar, organizar e acompanhar as informações do negócio.

Atualmente, diversas informações importantes dependem de controles manuais e do conhecimento da responsável pela empresa. A criação de uma estrutura de dados pode contribuir para organizar os pedidos, clientes, serviços, etapas do processo, prazos e pagamentos.

A partir dos problemas identificados, foram levantados requisitos funcionais e não funcionais e iniciada a identificação das entidades, atributos e relacionamentos necessários para representar o negócio.

As próximas etapas deverão validar as regras de negócio, finalizar as cardinalidades, consolidar o dicionário de dados e construir o DER, garantindo que o modelo seja consequência da análise realizada.

---

## Estrutura do projeto

```text
Projeto ERP - Santa Barbara/
│
├── 01 - Identificação da equipe/
├── 02 - Caracterização da empresa/
├── 03 - Justificativa das escolhas/
├── 04 - Problemas identificados/
├── 05 - Processos de negócio/
├── 06 - Requisitos funcionais/
├── 07 - Requisitos não funcionais/
├── 08 - Regras de negócio/
├── 09 - Restrições e políticas organizacionais/
├── 10 - Fluxogramas/
├── 11 - Entidades/
├── 12 - Atributos/
├── 13 - Relacionamentos/
├── 14 - Cardinalidades/
├── 15 - Dicionário de dados conceitual/
├── 16 - DER/
├── 17 - Justificativas técnicas/
└── 18 - Conclusão/
```
