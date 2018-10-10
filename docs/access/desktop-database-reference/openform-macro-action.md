---
title: Ação de Macro AbrirFormulário
TOCTitle: OpenForm Macro Action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba0314fff63014b36565b178f97950660ffec14f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464984"
---
# <a name="openform-macro-action"></a>Ação de Macro AbrirFormulário


**Aplica-se a**: Access 2013 | Office 2013


Você pode usar a ação **AbrirFormulário** para abrir um formulário no modo formulário, modo de Design, modo Visualizar impressão ou modo folha de dados. Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.

## <a name="setting"></a>Configuração

A ação **AbrirFormulário** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nome do formulário</strong></p></td>
<td><p>O nome do formulário a ser aberto. Caixa <strong>Nome do formulário</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros mostra todos os formulários no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirFormulário</strong> em um banco de dados biblioteca, o Microsoft Access procurará primeiro o formulário com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual o formulário será aberto. Clique em <strong>formulário</strong>, <strong>Design</strong>, <strong>Modo Visualizar impressão</strong>, <strong>folha de dados</strong>, <strong>tabela dinâmica</strong>ou <strong>gráfico dinâmico</strong> , na caixa <strong>Exibir</strong> . O padrão é <strong>formulário</strong>.</p>

> [!NOTE]
> <P>A definição do argumento <STRONG>Exibir</STRONG> substitui as configurações das propriedades de <STRONG>ModoPadrão</STRONG> e <STRONG>ViewsAllowed</STRONG> do formulário. Por exemplo, se a propriedade <STRONG>ViewsAllowed</STRONG> de um formulário é definida como <STRONG>folha de dados</STRONG>, você ainda pode usar a ação <STRONG>AbrirFormulário</STRONG> para abrir o formulário no modo formulário.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome do Filtro</strong></p></td>
<td><p>Um filtro que restringe ou classifica os registros do formulário. Você pode inserir o nome de uma consulta existente ou um filtro que foi salvo como uma consulta. No entanto, a consulta deve incluir todos os campos do formulário que você está abrindo ou ter sua propriedade <strong>OutputAllFields</strong> definida como <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condição Where</strong></p></td>
<td><p>Uma cláusula SQL WHERE válida (sem a palavra onde) ou expressão que o Access utiliza para selecionar registros do formulário da tabela ou consulta base. Se você selecionar um filtro com o argumento <strong>Nome do filtro</strong> , o Access aplica essa cláusula WHERE aos resultados do filtro. Para abrir um formulário e restringir seus registros àqueles especificados pelo valor de um controle em outro formulário, use a seguinte expressão: <strong>[</strong><em>fieldname</em><strong>] = formulários! [</strong> <em>formname</em> <strong>]! [</strong><em>controlname em outro formulário</em><strong>]</strong> substitua <em>fieldname</em> pelo nome de um campo na tabela ou consulta do formulário que você deseja abrir subjacente. Substitua o nome de outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros no primeiro formulário devem corresponder <em>formname</em> e <em>controlname em outro formulário</em> .</p>

> [!NOTE]
> <P>O comprimento máximo do argumento <STRONG>Condição Where</STRONG> é 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE complexa mais, maior que isso, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> no Visual Basic para módulo Applications (VBA) em vez disso. Você pode inserir instruções cláusula SQL WHERE de até 32.768 caracteres no VBA.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados para o formulário. Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros mas não pode editar registros existentes), <strong>Editar</strong> (o usuário pode editar registros existentes e adicionar novos registros), ou <strong>Somente leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>. <strong>Notes</strong></p>
<ul>
<li><p>A definição do argumento <strong>Modo de dados</strong> substitui as configurações das propriedades de <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e <strong>DataEntry</strong> do formulário. Por exemplo, se uma propriedade <strong>PermitirEdições</strong> formulário for definida como <strong>não</strong>, você ainda pode usar a ação <strong>AbrirFormulário</strong> para abrir o formulário no modo de edição.</p></li>
<li><p>Se você deixar este argumento em branco, o Access abre o formulário no modo de entrada de dados definido pelas propriedades de <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e <strong>DataEntry</strong> do formulário.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Modo Janela</strong></p></td>
<td><p>O modo de janela na qual o formulário é aberto. Clique em <strong>Normal</strong> (o formulário é aberto no modo definido pelas suas propriedades), <strong>oculto</strong> (o formulário é oculto), o <strong>ícone</strong> (o formulário é aberto minimizado como uma pequena barra de título na parte inferior da tela), ou <strong>diálogo</strong> (do formulário <strong>Modal</strong> e PopUp do <strong> </strong>propriedades são definidas como <strong>Sim</strong>). O padrão é <strong>Normal</strong>.</p>

> [!NOTE]
> <P>Algumas configurações do argumento <STRONG>Modo Janela</STRONG> não se aplicam ao usar documentos com guias. Para alternar para janelas sobrepostas:</P>


<p></p>
<ol>
<li><p>Clique na guia arquivo e clique em <strong>Opções</strong>.</p></li>
<li><p>Na caixa de diálogo <strong>Opções do Access</strong> , clique em <strong>Banco de dados atual</strong>.</p></li>
<li><p>Na seção <strong>Opções de aplicativo</strong>, em <strong>Opções da janela de documento</strong>, clique em <strong>Janelas sobrepostas</strong>.</p></li>
<li><p>Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em um formulário no painel de navegação, ou clicando o formulário no painel de navegação e selecionando um modo de exibição.

Um formulário pode ser modal (deve ser fechado ou oculto para que o usuário possa realizar qualquer outra ação) ou sem janela restrita (o usuário pode mover para outras janelas enquanto o formulário está aberto). Ele também pode ser um formulário pop-up (um formulário utilizado para reunir ou exibir informações que permanecem na parte superior de todas as outras janelas do Access). Você definir as propriedades **Modal** e **PopUp** quando você cria o formulário. Se você usar **Normal** para o argumento **Modo janela** , o formulário é aberto no modo especificado pelas configurações dessas propriedades. Se você usar a **caixa de diálogo** do argumento **Modo janela** , duas essas propriedades serão definidas como **Sim**. Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você mostra ou restaurá-lo.

Quando você abre um formulário com o argumento **Modo janela** definido como **diálogo**, o Access suspende a macro até que o formulário é fechado ou oculto. Você pode ocultar um formulário definindo sua propriedade **Visible** como **não** usando a ação **DefinirValor** .


> [!TIP]
> <P>Você pode selecionar um formulário no painel de navegação e arraste-o para uma linha de ação de macro. Isso cria automaticamente uma ação <STRONG>AbrirFormulário</STRONG> que abre o formulário no modo formulário.</P>



O filtro e a condição WHERE aplicados se tornam a configuração da propriedade **Filter** do formulário.

## <a name="examples"></a>Exemplos

**Definir o valor de um controle usando uma macro**

A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers. Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações. A ação **DefinirValor** define o controle de código do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores. A ação **GoToControl** , em seguida, move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Eco no</strong>: <strong>não</strong></p></td>
<td><p>Pare a atualização da tela enquanto a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p><strong>FecharJanela</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>Nome FormObject</strong>: lista de produto para <strong>Salvar</strong>: <strong>não</strong></p></td>
<td><p>Feche o formulário de lista de produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: produtos <strong>modo de exibição</strong>: <strong>Modo FormData</strong>: <strong>Modo AddWindow</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário Products.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [formulários]! [Produtos]! [SupplierID] <strong>Expressão</strong>: SupplierID</p></td>
<td><p>Defina o controle de código do fornecedor como o fornecedor atual no formulário fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID da categoria.</p></td>
</tr>
</tbody>
</table>


A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações. Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** . Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.

**Sincronizar formulários usando uma macro**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condição</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Eco no</strong>: <strong>não</strong></p></td>
<td><p>Pare a atualização da tela enquanto a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mover para o registro do fornecedor cujos produtos você deseja ver, em seguida, clique no botão Revisar produtos novamente. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecione um fornecedor</p></td>
<td><p>Se não houver nenhum fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: NomeDaEmpresa</p></td>
<td><p>Mova o foco para o controle NomeDaEmpresa.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Interrompa a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>da lista de produto: <strong>DatasheetFilter nome</strong>: <strong>condição onde</strong>: [SupplierID] = [formulários]! Fornecedores! [SupplierID] <strong>Modo de dados</strong>: <strong>Modo de OnlyWindow de leitura</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário de lista de produtos e mostram os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>Direita</strong>: 0.7799&quot; <strong>para baixo</strong>: 1,8&quot;</p></td>
<td><p>Posiciona o formulário de lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>

