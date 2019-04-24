---
title: Criar e personalizar um aplicativo Web no Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 628745f4-82e9-4838-9726-6f3e506a654f
localization_priority: Priority
ms.openlocfilehash: d7d27e98189a5b6784e4db48c81a545b85f01fc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306089"
---
# <a name="create-and-customize-a-web-app-in-access"></a>Criar e personalizar um aplicativo Web no Access

> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-BR/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
Access 2013 apresenta um novo modelo de aplicativo, que permite aos especialistas da área criar de forma rápida os aplicativos baseados na Web. Acompanha Access um conjunto de modelos que podem ser usados para promover a criação de aplicativos.

<a name="ac15_CreateAndCustomizeWebApp_Prerequisites"> </a>

## <a name="prerequisites-for-building-an-app-with-access-2013"></a>Pré-requisitos para a criação de um aplicativo no Access 2013

Para acompanhar as etapas deste exemplo, será necessário:
  
- Access
    
- Um ambiente de desenvolvimento do SharePoint
    
Para obter mais informações sobre como configurar o ambiente de desenvolvimento do SharePoint, confira [Configurar um ambiente de desenvolvimento geral para o SharePoint](https://docs.microsoft.com/sharepoint/dev/general-development/set-up-a-general-development-environment-for-sharepoint). 
  
Para saber mais sobre como obter o Access e o SharePoint, confira [Downloads](https://msdn.microsoft.com/office/apps/fp123627).

<a name="ac15_CreateAndCustomizeWebApp_CreateTheApp"> </a>

## <a name="create-the-app"></a>Criar o aplicativo

Imagine que você deseja criar um Access aplicativo que acompanha problemas em sua empresa. Antes de começar a criar as tabelas e vista do zero, você deve procurar um modelo de esquema que atenda às suas necessidades.
  
### <a name="to-create-the-issue-tracking-app"></a>Para criar o aplicativo de acompanhamento de problemas

1. Abra o Access e escolha a opção **Aplicativo da Web personalizado**.
    
2. Digite um nome e um local da Web para o aplicativo. É possível também escolher um local na lista **Locais** e escolher **Criar**.
    
3. Digite **Problemas** na caixa **O que deseja acompanhar?** e pressione ENTER. 
    
   Uma lista de modelos que podem ser úteis para o acompanhamento de problemas é exibida na Figura 1.
    
   **Figura 1. Modelos que correspondem à pesquisa de problemas**

   ![Modelos correspondentes à pesquisa de problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modelos correspondentes à pesquisa por problemas")
  
4. Escolha **Problemas**.
    
O Access cria um conjunto de tabelas e de modos de exibição.
  
## <a name="explore-the-app"></a>Explorar o aplicativo
<a name="ac15_CreateAndCustomizeWebApp_ExploreTheApp"> </a>

Para compreender se o esquema e os modos de exibição atendem às suas necessidades, será necessário testá-los.
  
As tabelas criadas por meio da seleção do esquema Problemas serão exibidas no Painel Bloco. As tabelas Problemas, Clientes e Funcionários são o objeto principal do aplicativo. A tabela Problemas armazena informações sobre cada problema. Cada problema é aberto e atribuído por um funcionário em nome de um cliente. As tabelas Problemas Relacionados e Comentários do Problema desempenham um papel de suporte no aplicativo. A tabela Problemas Relacionados permite a vinculação de um problema a outro. A tabela Comentários do Problema armazena vários comentários para um único problema.
  
Em um banco de dados de área de trabalho do Access (.accdb), os relacionamentos entre tabelas são gerenciados na janela **Relacionamentos**. Access 2013 Os aplicativos gerenciam os relacionamentos usando campos para definir o tipo de dados de **Pesquisa**. Teste os relacionamentos da tabela Problemas ao clicar com o botão direito de mouse no bloco **Problemas** e selecione **Editar Tabela**.
  
O campo **Cliente** está relacionado à tabela **Clientes**. Para testar os relacionamentos, selecione o campo **Cliente** e, em seguida, **Modificar Pesquisas**. O **Assistente de pesquisa** é exibido como na Figura 2. 
  
**Figura 2. O assistente de pesquisa exibindo a relação da tabela Clientes**

![Assistente de Pesquisa exibindo a relação](media/odc_Access15_CreateAndCustomizeWebApp_Figure02.jpg "Assistente de Pesquisa exibindo a relação")
  
A caixa de diálogo do assistente de pesquisa mostra que o campo **Cliente** está associado à tabela **Clientes** e para retornar ao campo **Nome para Exibição Nome Sobrenome** na tabela **Clientes**. 
  
Os campos **Aberto por**, **Atribuído por** e **Alterado por** estão relacionados à tabela **Funcionários**. Diversos outros campos também são definidos para o tipo de dados de **Pesquisa**. Nesses casos, o tipo de dados de pesquisa é usado para determinar os valores específicos a serem permitidos no campo. 
  
Feche a tabela **Problemas** e teste o Painel Bloco. Os três blocos superiores, para as tabelas **Problemas**, **Clientes** e **Funcionários** são exibidos de forma diferente em relação aos dois blocos inferiores, para as tabelas **Problemas Relacionados** e **Comentários do Problema**, como mostrado na Figura 3. 
  
**Figura 3. Painel Bloco para o esquema Problemas**

![Painel Bloco para o esquema Problemas](media/odc_Access15_CreateAndCustomizeWebApp_Figure03.jpg "Painel Bloco para o esquema de Problemas")
  
As tabelas **Problemas Relacionados** e **Comentários do Problema** estarão desativadas, pois devem ser ocultadas do usuário no navegador da Web. 
  
Use o aplicativo para acompanhar alguns problemas. Para isso, clique em **Iniciar aplicativo** para abri-lo no navegador da Web. 
  
O aplicativo vai abrir a exibição **Lista de Problemas** da tabela Problemas. Antes de adicionar um problema, convém adicionar alguns clientes e funcionários. Clique no bloco **Clientes** para começar a adicioná-los. 
  
Use o Seletor de Modo de Exibição para escolher um entre os três disponíveis para a tabela **Clientes**, rotulados como **Lista**, **Folha de Dados** e **Grupos**, como mostrado na Figura 4. 
  
**Figura 4. Seletor de Modo de Exibição**

![Seletor de Modo de Exibição](media/odc_Access15_CreateAndCustomizeWebApp_Figure04.jpg "Seletor de Modo de Exibição")
  
Escolher **Lista** vai ativar o modo de exibição de **Lista de Clientes**, que é um modo de exibição de Detalhes da Lista. Detalhes da Lista é um dos modos de exibição Access gerados automaticamente quando você criar uma tabela. A principal característica que distingue o modo de exibição Detalhes da Lista é o painel de Lista exibido ao lado esquerdo da exibição. Esse painel é usado para filtrar e para navegar entre os registros no modo de exibição. Em um Access banco de dados de área de trabalho, implementar um modo de exibição de lista pesquisável exige um código escrito personalizado. 
  
Escolher a **Folha de Dados** abrirá o modo de exibição **Folha de Dados de Clientes**. A Folha de Dados é outro tipo de visualização que o Access gera automaticamente quando cria uma tabela. Os modos de exibição de Folha de Dados são úteis para quem considerar mais fácil inserir, classificar e filtrar dados, como se o fizesse em uma planilha. 
  
Escolher Grupos abrirá o Modo de Exibição de Resumo. Esse recurso pode ser usado para agrupar registros baseados em um campo e, opcionalmente, poderá calcular uma soma ou uma média.
  
À medida que adicionar clientes, use a Barra de Ações para adicionar, editar, salvar e excluir registros, além de cancelar edições. A Barra de Ações é uma barra de ferramentas personalizável, exibida na parte superior dos modos de exibição, como mostrado na Figura 5.
  
**Figura 5. Barra de Ações**

![Barra de Ações](media/odc_Access15_CreateAndCustomizeWebApp_Figure05.jpg "Barra de Ações")
  
Ao adicionar alguns clientes e funcionários, abra o modo de exibição Lista de Problemas e comece a adicionar problemas. À medida que você digitar o nome de um cliente na caixa Cliente, serão exibidos um ou mais nomes de clientes, como mostrado na Figura 6.
  
**Figura 6. Controle de Preenchimento Automático**

![Controle de Preenchimento Automático](media/odc_Access15_CreateAndCustomizeWebApp_Figure06.jpg "Controle de Preenchimento Automático")
  
A caixa Cliente é um controle de preenchimento automático. Esse controle exibe uma lista de registros que correspondem ao que você estiver digitando dentro da caixa. Isso ajuda a garantir a precisão da entrada de dados.
  
## <a name="customize-the-app"></a>Personalizar o aplicativo
<a name="ac15_CreateAndCustomizeWebApp_CustomizeTheApp"> </a>

Agora que você está familiarizado com o aplicativo, observe que o modo de exibição Lista de Problemas não inclui as informações de contato dos clientes. Personalize o aplicativo para adicionar o telefone comercial do cliente à tabela Problemas, à medida que o problema for criado.
  
### <a name="to-add-a-field-to-the-issues-table"></a>Para adicionar um campo à tabela Problemas

1. Abra o aplicativo no Access.
    
2. Selecione o bloco **Problemas**, escolha o ícone **Configurações/Ações** e selecione **Editar Tabela**.
    
3. Digite o **Número de Contato** na primeira célula em branco, na coluna **Nome do Campo**. 
    
4. Escolha **Texto Curto** na coluna **Tipo de Dados**. 
    
5. Escolha **Salvar**.
    
6. Feche a tabela Problemas.
    
Agora que você já tem um campo para armazenar o número de telefone, crie uma macro de dados para pesquisar as informações do contato.
  
### <a name="to-create-the-data-macro-to-look-up-contact-information"></a>Como criar a macro de dados para pesquisar informações de contato

1. No grupo **Criar**, selecione **Avançado** e escolha **Macro de Dados**.
    
2. Escolha **Criar Parâmetro**.
    
3. Na caixa **Nome**, digite **CustID**. Na lista suspensa **Tipo**, escolha **Número (Decimal Flutuante).**
    
4. Na lista suspensa **Adicionar Nova Ação**, escolha **LookupRecord**. 
    
5. Na lista suspensa **Pesquisar Novo Registro em**, escolha **Clientes**. 
    
6. Na caixa **Condição Where**, digite **[Clientes].[ID]=[CustID]**. 
    
7. Escolha **SetReturnVar** na lista suspensa **Adicionar Nova Ação**. 
    
    > [!NOTE]
    > Serão exibidas duas listas suspensas **Adicionar Nova Ação**, uma dentro do bloco **LookupRecord** e outra fora **dele**. É necessário escolher a lista suspensa **Adicionar Nova Ação** dentro do bloco **LookupRecord**, como descrito na Figura 7. 
  
   **Figura 7. Lista suspensa Adicionar Nova Ação**

   ![Lista suspensa Adicionar Nova Ação](media/odc_Access15_CreateAndCustomizeWebApp_Figure07.jpg "Lista suspensa Adicionar Nova Ação")
  
8. Na caixa **Nome**, digite **ContactPhone**. 
    
9. Na caixa **Expressão**, digite **[Clientes].[Telefone Comercial]**. 
    
10. Selecione **Salvar**. Digite **GetContactPhone** na caixa **Nome da Macro** e clique em **OK**.
    
    A macro deverá ser semelhante à macro exibida na Figura 8.
    
    **Figura 8. Macro de dados GetContactPhone**

    ![Macros de dados GetContactPhone](media/odc_Access15_CreateAndCustomizeWebApp_Figure08.jpg "Macros de dados GetContactPhone")
  
11. Feche o Modo Design da macro.
    
Agora você está pronto para adicionar o campo **Número de Contato** ao formulário Lista de Problemas. 
  
### <a name="to-add-the-contact-number-field-to-the-issues-list-form"></a>Para adicionar o campo Número de Contato ao formulário Lista de Problemas

1. Selecione a tabela **Problemas**. Desse modo, o formulário Lista de Problemas será selecionado. 
    
2. No Seletor de Modo de Exibição, selecione **Lista**, clique no ícone **Configurações/Ações** e escolha **Editar**.
    
3. Arraste o campo **Número de Contato** do painel **Lista do Campo** para o local do formulário no qual deseja que o número de contato seja exibido. 
    
4. Selecione a caixa de texto **Número de Contato** e clique em **Dados**. 
    
5. Na caixa **Nome do Controle**, digite **CustomerContact** e feche o menu pop-up **Dados**. 
    
6. Escolha **Salvar**.
    
Agora é necessário escrever uma macro de interface do usuário (UI), que copiará o campo **Telefone Comercial**, da tabela **Clientes** para o campo **Telefone de Contato** da tabela **Problemas**. O evento **After Update** do controle **CustomerAutocomplete** é um bom local para a macro. 
  
### <a name="to-create-the-afterupdate-macro"></a>Para criar uma macro AfterUpdate

1. Escolha o controle **CustomerAutocomplete**, selecione o botão **Ações** e clique em **Após Atualização**. 
    
    Uma macro em branco será aberta no Modo Design de macro.
    
2. Na lista suspensa **Adicionar Nova Ação**, escolha **RunDataMacro**. 
    
3. Na lista suspensa **Nome da macro**, escolha **GetContactPhone**. 
    
4. Na caixa **CustID**, digite **[CustomerAutocomplete]**. 
    
5. Na caixa **SetLocalVar**, digite **Phone**. 
    
    Quando você escolhe a macro de dados GetContactPhone criada anteriormente, o Access preenche automaticamente no nome do parâmetro e retorna variáveis para a macro.
    
    O número de telefone do cliente será armazenado em uma variável chamada Telefone.
    
6. A partir da lista suspensa **Adicionar Nova Ação**, escolha **SetProperty**. 
    
7. Na caixa **Nome do Controle**, digite **CustomerContact**. 
    
8. Na lista suspensa **Propriedades**, escolha **Valor**. 
    
9. Na caixa **Valor**, digite **=[Phone]**. 
    
10. Escolha **Salvar**.
    
    A macro deverá ser semelhante à macro exibida na Figura 9.
    
    **Figura 9. Macro Após Atualização**

    ![Macro Após Atualização](media/odc_Access15_CreateAndCustomizeWebApp_Figure09.jpg "Macro Após Atualização")
  
11. Feche o Modo Design da macro.
    
12. Feche o modo de exibição Lista de Problemas. Escolha **Sim**, quando for solicitado que você salve as alterações. 
    
Agora estamos prontos para testar a personalização. Clique em **Iniciar Aplicativo** para abrir o aplicativo no navegador da web e adicionar um problema novo. A caixa **Número de Contato** será atualizada automaticamente depois que o nome do cliente for digitado, como mostra a Figura 10. 
  
**Figura 10. O modo de exibição Problemas atualizado com o número de telefone**

![O modo de exibição Problemas atualizado com o número de telefone](media/odc_Access15_CreateAndCustomizeWebApp_Figure10.jpg "O modo de exibição Problemas atualizado com o número de telefone")
  
## <a name="conclusion"></a>Conclusão

Usar um dos modelos de esquema que acompanham o é uma boa maneira de promover a criação de um Access aplicativo da Web. Os modos de exibição criados automaticamente por você contêm funcionalidades avançadas que exigem a implementação de código personalizado em um banco de dados de área de trabalho do Access. 
  
## <a name="see-also"></a>Confira também

- [Novidades para os desenvolvedores do Access 2013](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx) 
- [Referência de aplicativo Web personalizado do Access](access-custom-web-app-reference.md)
  

