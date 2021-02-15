---
title: Ação da macro AbrirFormulário
TOCTitle: OpenForm macro action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf89b61a65c11f09d5a07e52caeee5ad416c118a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288368"
---
# <a name="openform-macro-action"></a>Ação da macro AbrirFormulário

**Aplica-se ao:** Access 2013, Office 2013

You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view. Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.

## <a name="setting"></a>Setting

A **ação OpenForm** tem os seguintes argumentos.

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
<td><p>O nome do formulário a ser aberto. A <strong>caixa Nome do</strong> Formulário na seção <strong>Argumentos da</strong> Ação do painel Construtor de Macros mostra todos os formulários no banco de dados atual. Este é um argumento obrigatório. Se você executar uma macro contendo a ação <strong>OpenForm</strong> em um banco de dados biblioteca, o Microsoft Access primeiro procura o formulário com esse nome no banco de dados biblioteca e, em seguida, no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O exibição no qual o formulário será aberto. Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. O padrão é <strong>Form</strong>.</p><p><strong>OBSERVAÇÃO:</strong>a <STRONG>configuração</STRONG> do argumento View substitui as configurações das propriedades <STRONG>DefaultView</STRONG> e <STRONG>ViewsAllowed do</STRONG> formulário. For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome do Filtro</strong></p></td>
<td><p>Um filtro que restringe ou classifica os registros do formulário. Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta. No entanto, a consulta deve incluir todos os campos no formulário que você está abrindo ou ter sua <strong>propriedade OutputAllFields</strong> definida como <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condição Where</strong></p></td>
<td><p>Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou expressão que o Access usa para selecionar registros da tabela ou consulta base do formulário. Se você selecionar um filtro com o argumento <strong>Nome do Filtro</strong>, o Access aplicará essa cláusula WHERE aos resultados do filtro. Para abrir um formulário e restringir seus registros àqueles especificados pelo valor de um controle em outro formulário, use a expressão a seguir: <strong>[</strong><em>nome_do_campo</em><strong>] = Formulários![</strong> <em>formname</em><strong>]! [</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open. Substitua <em>formname</em> e <em>controlname em outro</em> formulário pelo nome do outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros do primeiro formulário sejam match.</p><p><strong>OBSERVAÇÃO:</strong>o comprimento máximo do argumento <STRONG>Condição Where</STRONG> é de 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE mais complexa do que essa, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> em um módulo do VBA (Visual Basic for Applications). É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados do formulário. Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>. <strong>Anotações</strong></p>
<ul>
<li><p>A <strong>configuração</strong> do argumento Modo de Dados substitui as configurações das propriedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>e <strong>DataEntry do</strong> formulário. For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</p></li>
<li><p>Se você deixar esse argumento em branco, o Access abrirá o formulário no modo de entrada de dados definido pelas propriedades <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>e <strong>DataEntry</strong> do formulário.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Modo Janela</strong></p></td>
<td><p>O modo de janela no qual o formulário é aberto. Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>). O padrão é <strong>Normal</strong>.</p><p><strong>OBSERVAÇÃO:</strong>algumas <STRONG>configurações de</STRONG> argumento do Modo Janela não se aplicam ao usar documentos com guias. Para alternar para janelas sobrepostas:</p>
<ol>
<li><p>Clique na guia Arquivo e em <strong>Opções.</strong></p></li>
<li><p>Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</p></li>
<li><p>Na seção <strong>Opções de Aplicativo,</strong>em <strong>Opções de Janela de Documento,</strong>clique <strong>em Sobreposição do Windows</strong>.</p></li>
<li><p>Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em um formulário no Painel de Navegação ou clicar com o botão direito do mouse no formulário no Painel de Navegação e selecionar um modo de exibição.

Um formulário pode ser modal (deve ser fechado ou oculto antes que o usuário possa executar qualquer outra ação) ou sem janelas (o usuário pode se mover para outras janelas enquanto o formulário estiver aberto). Também pode ser um formulário pop-up (um formulário usado para coletar ou exibir informações que permanecem sobre todas as outras janelas do Access). Você pode definir **as propriedades Modal** **e PopUp** ao criar o formulário. Se você usar **Normal** para o **argumento Modo janela,** o formulário abre no modo especificado por essas configurações de propriedade. Se você usar **Dialog** para o **argumento Modo Janela,** essas propriedades serão definidas como **Sim**. Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você o mostra ou restaura.

Quando você abre um formulário com o argumento **Modo** Janela definido como **Diálogo,** o Access suspende a macro até que o formulário seja fechado ou oculto. Você pode ocultar um formulário definindo **sua propriedade Visible** como **Não** usando a **ação SetValue.**

> [!TIP]
> Você pode selecionar um formulário no Painel de Navegação e arrastá-lo para uma linha de ação de macro. This automatically creates an **OpenForm** action that opens the form in Form view.

O filtro e a condição WHERE aplicados tornam-se a definição da propriedade **Filter do** formulário.

## <a name="examples"></a>Exemplos

**Definir o valor de um controle, usando uma macro**

A macro a seguir abre o formulário Adicionar Produtos de um botão no formulário de Fornecedores. Mostra o uso das ações **Echo**, **CloseWindow**, **OpenForm**, **SetValue** e **GoToControl**. A **ação SetValue** define o controle de ID do Fornecedor no formulário Produtos para o fornecedor atual no formulário Fornecedores. A **ação IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve estar anexada ao botão Adicionar Produtos no formulário de Fornecedores.

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
<td><p><strong>Echo On</strong>: <strong>No</strong></p></td>
<td><p>Interrompe a atualização de tela quando a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p><strong>CloseWindow</strong></p></td>
<td><p><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></p></td>
<td><p>Fecha o Formulário de Lista de Produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></p></td>
<td><p>Abre o formulário de produtos.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</p></td>
<td><p>De definir o controle de ID de fornecedor para o fornecedor atual no formulário Fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Control Name</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID da categoria.</p></td>
</tr>
</tbody>
</table>


A macro a seguir abre um formulário de Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual. Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.** Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.** Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.

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
<th><p>Condition</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos: Configuração</p></th>
<th><p>Comentário</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Echo</strong></p></td>
<td><p><strong>Echo On</strong>: <strong>No</strong></p></td>
<td><p>Interrompe a atualização de tela quando a macro é executada.</p></td>
</tr>
<tr class="even">
<td><p>IsNull([SupplierID])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>vá para o registro do fornecedor cujos produtos você deseja ver e clique no botão Revisar Produtos novamente. <strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</p></td>
<td><p>Se não houver fornecedor atual no formulário Fornecedores, exibe uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mova o foco para o controle CompanyName.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Pare a macro.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: Exibição de Lista <strong>de</strong>Produtos : <strong>Nome do Filtro de</strong>Folha de Dados : <strong>Condição</strong>Onde : [SupplierID] = [Forms]! [Fornecedores]! [SupplierID] <strong>Modo de Dados</strong>: <strong>Ler Modo Somente Janela</strong>: <strong>Normal</strong></p></td>
<td><p>Abra o formulário Lista de Produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>MoveAndSizeWindow</strong></p></td>
<td><p><strong>À</strong>direita: 0,7799 &quot; <strong>para baixo:</strong>1,8&quot;</p></td>
<td><p>Posiciona o formulário Lista de Produtos no canto inferior direito do formulário Fornecedores.</p></td>
</tr>
</tbody>
</table>

