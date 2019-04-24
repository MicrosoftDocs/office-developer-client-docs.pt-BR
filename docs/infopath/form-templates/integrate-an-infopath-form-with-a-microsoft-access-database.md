---
title: Integrar um formulário do InfoPath a um banco de dados do Microsoft Access
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ec9a9c0-b348-4a31-b377-e95db2f92455
description: O Microsoft InfoPath dá suporte ao uso de um banco de dados do Microsoft Access 2010 como a fonte de dados primária para um formulário, ou como uma fonte de dados secundária para um formulário ou controle. Este artigo explica como usar um banco de dados do Access 2010 como uma fonte de dados.
ms.openlocfilehash: dbc39e0d0908214904d77b8955f3d231f0bfb20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303511"
---
# <a name="integrate-an-infopath-form-with-a-microsoft-access-database"></a>Integrar um formulário do InfoPath a um banco de dados do Microsoft Access

O Microsoft InfoPath dá suporte ao uso de um banco de dados do Microsoft Access 2010 como a fonte de dados primária para um formulário, ou como uma fonte de dados secundária para um formulário ou controle. Este artigo explica como usar um banco de dados do Access 2010 como uma fonte de dados.
  
## <a name="using-a-microsoft-access-database-as-a-data-source"></a>Usando um banco de dados do Microsoft Access como fonte de dados

### <a name="setting-up-a-microsoft-access-database-as-a-forms-primary-data-source"></a>Configurando um banco de dados do Microsoft Access Database como a fonte de dados principal de um formulário

As conexões de banco de dados são estabelecidas no InfoPath usando o **Assistente de Conexão de Dados**. Esse assistente é aberto selecionando **Banco de Dados** na seção **Modelos de Formulário Avançados** na guia **Novo** do Microsoft Office Backstage e então clicando em **Criar Este Formulário**.
  
Ao clicar em **Selecionar Banco de Dados**, você poderá escolher uma fonte de dados existente ou se conectar diretamente a um arquivo de banco de dados específico.
  
Depois de selecionar um banco de dados, o assistente solicitará que você selecione uma tabela do banco de dados a ser usado como a fonte de dados para o formulário. À medida que você adiciona tabelas, os relacionamentos das tabelas umas com as outras serão estabelecidos, e o assistente exibirá as tabelas e os relacionamentos hierárquicos na lista **Estrutura da fonte de dados**. Se você marcar a caixa de seleção **Mostrar colunas da tabela**, o assistente exibirá os nomes de campo de cada tabela na lista Estrutura da fonte de dados; use as caixas de seleção ao lado de cada campo para especificar se um campo será incluído na instrução SQL criada pelo assistente. 
  
> [!NOTE]
> [!OBSERVAçãO] Os campos de chave primária de cada tabela sempre estarão selecionados e não podem ser removidos. 
  
Quando as tabelas, os relacionamentos e os campos tiverem sido especificados usando o **Assistente de Conexão de Dados**, você poderá clicar em **Editar SQL** para exibir a instrução SQL que será usada para estabelecer a fonte de dados para o formulário. Na caixa de diálogo **Editar SQL**, é possível clicar em **Testar Instrução SQL** para verificar se o InfoPath conseguirá criar a fonte de dados das informações fornecidas. Também é possível usar a caixa de diálogo **Editar SQL** para modificar a instrução SQL para criar consultas mais complexas. 
  
> [!NOTE]
> [!OBSERVAçãO] As instruções SQL usadas pelo InfoPath são consultas de modelagem de dados. As consultas de modelagem de dados permitem a criação de relacionamentos hierárquicos entre duas ou mais entidades lógicas. É possível usar instruções JOIN SQL, mas isso não é recomendável, porque fazer isso desabilitará o envio de formulários. Para saber mais sobre consultas de modelagem de dados, consulte a documentação no Microsoft Developer Network (MSDN). 
  
A última página do **Assistente de Conexão de Dados** exibe informações de resumo sobre a fonte de dados, incluindo o nome e o local do arquivo da fonte de dados, o nome da tabela pai primária, o número de tabelas usadas e o status de envio. O status de envio diz a você se a instrução SQL gerada permitirá o envio de dados bem-sucedido para a fonte de dados. 
  
### <a name="setting-up-a-microsoft-access-database-as-a-secondary-data-source"></a>Configurando um banco de dados do Microsoft Access como uma fonte de dados secundária

As fontes de dados secundárias podem ser usadas para fornecer as entradas para uma caixa de listagem ou uma caixa de lista suspensa, ou você pode escrever código para adicionar dados de uma fonte de dados secundária para seu formulário. Para trabalhar com fontes de dados secundárias em seu formulário, clique em **Conexões de Dados** na guia **Dados** ao projetar um formulário. 
  
Quando você iniciar o **Assistente de Conexão de Dados**, será solicitado que você selecione se deseja receber dados para usá-los no formulário ou enviar dados no formulário. Escolha **Receber dados** e então clique em **Avançar**. Para criar uma fonte de dados secundária de um banco de dados, selecione **Banco de Dados (somente Microsoft SQL Server ou Microsoft Office Access)**. Na próxima página do assistente, clique em **Selecionar Banco de Dados** para escolher uma fonte de dados existente ou conecte-se diretamente a um arquivo de banco de dados específico. 
  
Depois de selecionar um banco de dados, o assistente solicitará a seleção de uma tabela ou consulta do banco de dados a ser usada como a fonte de dados do formulário. Você deve selecionar uma tabela ou consulta para começar, mas poderá selecionar tabelas adicionais posteriormente se quiser incluí-las. Depois de selecionar uma tabela ou consulta, o assistente permitirá que você selecione os campos que deseja usar na lista **Estrutura da fonte de dados**. Por padrão, todos os campos da tabela são selecionados, mas é possível remover campos se eles não forem necessários para seu formulário. Você também pode controlar como os registros retornados da tabela são classificados e se vários registros são permitidos. Para fazer isso, clique em **Modificar Tabela** e então selecione até três critérios de classificação na caixa de seleção **Ordem de Classificação**. Quando estiver satisfeito, clique em **Concluir**.
  
> [!NOTE]
> [!OBSERVAçãO] Os campos de chave primária de cada tabela sempre estarão selecionados e não podem ser removidos. 
  
O InfoPath também permite que você recupere dados de várias tabelas ou consultas ao mesmo tempo. Quando você recupera dados de várias tabelas ou consultas, deve ser capaz de estabelecer um relacionamento entre todas as tabelas ou consultas envolvidas com a tabela ou consulta original selecionada no **Assistente de Conexão de Dados**. Por exemplo, se for preciso recuperar dados da tabela Clientes do banco de dados Northwind, você poderá adicionar a tabela Pedidos para recuperar dados sobre todos os pedidos para aquele cliente e poderá adicionar a tabela Detalhes do Pedido para recuperar os detalhes de cada pedido.
  
Para adicionar outra tabela à fonte de dados, selecione a tabela que você deseja adicionar a uma tabela filha à lista **Estrutura da fonte de dados** e então clique em **Adicionar Tabela**. Selecione a tabela ou a consulta que você deseja adicionar e então clique em **Avançar**. O InfoPath solicita que você selecione o relacionamento ou os relacionamentos que deseja usar. Se campos das duas tabelas tiverem o mesmo nome, o InfoPath adicionará automaticamente esses campos como um relacionamento; caso contrário, ou se você não quiser usar um relacionamento personalizado, poderá clicar em **Adicionar Relacionamento** para especificar quais campos da tabela pai correspondem aos campos da tabela filha. Também é possível remover relacionamentos existentes clicando em **Remover Relacionamento** na caixa de diálogo **Editar Relacionamento**. 
  
Quando estiver satisfeito com os relacionamentos, clique em **Concluir**. Assim como acontece com a tabela principal, você pode especificar quais campos serão retornados da tabela filha. No entanto, você não pode usar o botão **Modificar Tabela** para editar a ordem na qual os registros são retornados. 
  
Quando as tabelas, os relacionamentos e os campos tiverem sido especificados, você poderá clicar em **Editar SQL** para exibir a instrução da consulta SQL que será usada para estabelecer a fonte de dados para o formulário. Na caixa de diálogo **Editar SQL**, você pode clicar em **Testar Instrução SQL** para verificar se o InfoPath poderá criar a fonte de dados desde as informações fornecidas. Também é possível usar a caixa de diálogo **Editar SQL** para modificar a instrução SQL para criar consultas mais complexas. 
  
> [!NOTE]
> As instruções SQL usadas pelo InfoPath são consultas de modelagem de dados. As consultas de modelagem de dados permitem a criação de relacionamentos hierárquicos entre duas ou mais entidades lógicas. É possível usar instruções JOIN SQL, mas isso não é recomendável, porque fazer isso desabilitará o envio de formulários. Para saber mais sobre consultas de modelagem de dados, consulte a documentação no Microsoft Developer Network (MSDN). 
  
## <a name="enabling-form-submission"></a>Habilitando o envio de formulários

Além do recebimento de dados de um banco de dados do Access, o InfoPath pode enviar dados novos ou alterados de volta para o banco de dados. Quando você usa o comando **Enviar** na guia **Início** ou o Microsoft Office Backstage para enviar alterações para o banco de dados, o InfoPath usa ADO (ActiveX Data Objects) para atualizar os registros no banco de dados. O envio de formulário será habilitado quando todas as condições a seguir forem atendidas: 
  
- Deve haver uma coluna base para todas as colunas usadas na consulta do formulário.
    
- Talvez uma coluna de tabela não apareça várias vezes na consulta inteira.
    
- Uma chave primária, uma restrição exclusiva ou um índice exclusivo deve estar disponível para todas as tabelas em uma cláusula SELECT usada na consulta do formulário.
    
- Uma tabela não pode ser incluída várias vezes na consulta do formulário.
    
- Os relacionamentos entre as tabelas principais e secundárias devem incluir todas as colunas de chave primária da tabela pai.
    
- Só pode haver uma tabela base para todas as colunas em uma cláusula SELECT usada na consulta do formulário.
    
Existem algumas circunstâncias sob as quais o InfoPath não pode enviar alterações de formulário para um banco de dados. Por exemplo, se você criar um formulário que retire dados de uma consulta em vez de uma tabela, ou se você personalizar a instrução SQL usada pelo InfoPath para incluir uma instrução JOIN, o InfoPath não poderá enviar alterações. Outra circunstância que impediria que o InfoPath enviasse alterações seria adicionar tabelas ao formulário que tem um relacionamento muitos para um com a tabela principal delas. Em situações onde o InfoPath não consegue enviar alterações para o banco de dados, o campo **Status de envio** na última página do **Assistente de Conexão de Dados** exibirá o motivo para a limitação. 
  

