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

Você pode usar a ação **AbrirFormulário** para abrir um formulário no modo formulário, modo de design, visualização de impressão ou modo folha de de formulários. Você pode selecionar a entrada de dados e os modos de janela para o formulário e restringir os registros que o formulário exibe.

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
<td><p>O nome do formulário a ser aberto. A caixa <strong>nome do formulário</strong> na seção argumentos da <strong>ação</strong> do painel Construtor de macros mostra todos os formulários no banco de dados atual. É um argumento obrigatório. Se você executar uma macro que contém a ação <strong>AbrirFormulário</strong> em um banco de dados biblioteca, o Microsoft Access procurará o formulário com esse nome primeiro no banco de dados biblioteca e depois no banco de dados atual.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>O modo de exibição no qual o formulário será aberto. Clique em <strong>formulário</strong>, <strong>design</strong>, <strong>Visualizar impressão</strong>, <strong>folha</strong>de data, <strong>tabela dinâmica</strong>ou <strong>gráfico dinâmico</strong> na caixa <strong>modo de exibição</strong> . O padrão é <strong>Form</strong>.</p><p><strong>Observação</strong>: a configuração do argumento <STRONG>Exibir</STRONG> substitui as configurações das propriedades <STRONG>ModoPadrão</STRONG> e <STRONG>ModosPermitidos</STRONG> do formulário. Por exemplo, se a propriedade <STRONG>ModosPermitidos</STRONG> de um formulário estiver definida como <STRONG>folha</STRONG>de a, você ainda poderá usar a ação <STRONG>AbrirFormulário</STRONG> para abrir o formulário no modo formulário.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Nome do Filtro</strong></p></td>
<td><p>Um filtro que restringe ou classifica os registros do formulário. Você pode digitar o nome de uma consulta existente ou de um filtro que foi salvo como consulta. No enTanto, a consulta deve incluir todos os campos no formulário que você está abrindo ou ter a propriedade <strong>OutputAllFields</strong> definida como <strong>Sim</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Condição Where</strong></p></td>
<td><p>Uma cláusula SQL WHERE válida (sem a palavra WHERE) ou expressão que o Access usa para selecionar registros da tabela ou consulta base do formulário. Se você selecionar um filtro com o argumento <strong>Nome do Filtro</strong>, o Access aplicará essa cláusula WHERE aos resultados do filtro. Para abrir um formulário e restringir seus registros aos especificados pelo valor de um controle em outro formulário, use a seguinte expressão: <strong>[</strong><em>FieldName</em><strong>] = Forms! [</strong> <em>FormName</em> <strong>]! [</strong><em>ControlName em outro formulário</em><strong>]</strong> substitui <em>FieldName</em> pelo nome de um campo na tabela ou consulta base do formulário que você deseja abrir. Substitua <em>FormName</em> e <em>ControlName em outro formulário</em> com o nome do outro formulário e o controle no outro formulário que contém o valor que você deseja que os registros no primeiro formulário correspondam.</p><p><strong>Observação</strong>: o comprimento máximo do argumento <STRONG>condição onde</STRONG> é de 255 caracteres. Se você precisar inserir uma cláusula SQL WHERE mais complexa e maior que isso, use o método <STRONG>OpenForm</STRONG> do objeto <STRONG>DoCmd</STRONG> em um módulo do Visual Basic for Applications (VBA). É possível inserir instruções de cláusulas SQL WHERE de até 32.768 caracteres no VBA.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Modo de Dados</strong></p></td>
<td><p>O modo de entrada de dados do formulário. Isso se aplica apenas aos formulários abertos no modo Formulário ou no modo Folha de Dados. Clique em <strong>Adicionar</strong> (o usuário pode adicionar novos registros, mas não pode editar os existentes), <strong>Editar</strong> (o usuário pode editar os registros existentes e adicionar novos) ou <strong>Somente Leitura</strong> (o usuário só pode exibir registros). O padrão é <strong>Editar</strong>. <strong>Anotações</strong></p>
<ul>
<li><p>A configuração do argumento <strong>modo de dados</strong> substitui as configurações das propriedades <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e DataEntry do formulário. <strong></strong> Por exemplo, se a propriedade <strong>PermitirEdições</strong> de um formulário estiver definida como <strong>não</strong>, você ainda poderá usar a ação <strong>AbrirFormulário</strong> para abrir o formulário no modo de edição.</p></li>
<li><p>Se você deixar este argumento em branco, o Access abrirá o formulário no modo de entrada de dados definido pelas propriedades <strong>PermitirEdições</strong>, <strong>PermitirExclusões</strong>, <strong>PermitirAdições</strong>e DataEntry do formulário. <strong></strong></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Modo Janela</strong></p></td>
<td><p>O modo de janela em que o formulário é aberto. Clique em <strong>normal</strong> (o formulário é aberto no modo definido por suas propriedades) <strong>, oculto</strong> (o formulário é oculto), <strong>ícone</strong> (o formulário abre minimizado como uma pequena barra de título na parte inferior da tela) ou <strong>caixa de diálogo</strong> (a <strong>janela restrita</strong> e o <strong>pop-up do formulário </strong>propriedades estão definidas como <strong>Sim</strong>). O padrão é <strong>Normal</strong>.</p><p><strong>Observação</strong>: algumas configurações de argumento do <STRONG>modo de janela</STRONG> não se aplicam ao usar documentos com guias. Para alternar para janelas sobrepostas:</p>
<ol>
<li><p>Clique na guia arquivo e em <strong>Opções</strong>.</p></li>
<li><p>Na caixa de diálogo <strong>Opções do Access</strong>, clique em <strong>Banco de Dados Atual</strong>.</p></li>
<li><p>Na seção <strong>Opções do aplicativo</strong>, em <strong>Opções da janela de documento</strong>, clique em janelas sobrepostas. <strong></strong></p></li>
<li><p>Clique em <strong>OK</strong> e feche e abra o banco de dados novamente.</p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Esta ação é semelhante a clicar duas vezes em um formulário no painel de navegação ou clicar com o botão direito do mouse no formulário no painel de navegação e selecionar um modo de exibição.

Um formulário pode ser de janela restrita (deve ser fechado ou oculto para que o usuário possa executar qualquer outra ação) ou sem janela restrita (o usuário pode mover para outras janelas enquanto o formulário está aberto). Também pode ser um formulário pop-up (um formulário usado para coletar ou exibir informações que permanecem na parte superior de todas as outras janelas do Access). Você define as propriedades **modal** e **Popup** quando cria o formulário. Se você usar **normal** para o argumento **modo janela** , o formulário é aberto no modo especificado por essas configurações de propriedade. Se você usar a **caixa de diálogo** do argumento **modo janela** , essas propriedades serão definidas como **Sim**. Um formulário aberto como oculto ou como um ícone retorna ao modo especificado por suas configurações de propriedade quando você o exibe ou restaura.

Quando você abre um formulário com o argumento **modo janela** definido como **caixa de diálogo**, o Access suspende a macro até que o formulário seja fechado ou oculto. Você pode ocultar um formulário definindo sua propriedade **Visible** como **não** usando a ação **DefinirValor** .

> [!TIP]
> Você pode selecionar um formulário no painel de navegação e arrastá-lo para uma linha de ação de macro. Isso cria automaticamente uma ação **AbrirFormulário** que abre o formulário no modo formulário.

O filtro e a condição WHERE aplicados tornam-se a configuração da propriedade **Filter** do formulário.

## <a name="examples"></a>Exemplos

**Definir o valor de um controle usando uma macro**

A macro a seguir abre o formulário Adicionar produtos a partir de um botão no formulário fornecedores. Ela mostra o uso das ações **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **IrParaControle** . A ação **DefinirValor** define o controle de ID do fornecedor no formulário produtos como o fornecedor atual no formulário fornecedores. A ação **IrParaControle** move o foco para o campo ID da categoria, onde você pode começar a inserir dados para o novo produto. Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.

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
<td><p><strong>Echo ativado</strong>: <strong>não</strong></p></td>
<td><p>Interrompa a atualização da tela enquanto a macro estiver em execução.</p></td>
</tr>
<tr class="even">
<td><p><strong>FecharJanela</strong></p></td>
<td><p><strong>Tipo de objeto</strong>: <strong>nome</strong>do formObject: <strong>salvamento</strong>da lista de produtos: <strong>não</strong></p></td>
<td><p>Feche o formulário lista de produtos.</p></td>
</tr>
<tr class="odd">
<td><p><strong>OpenForm</strong></p></td>
<td><p><strong>Nome do formulário</strong>: modo de <strong>exibição</strong>de produtos: <strong>modo FormData</strong>: <strong>modo AddWindow</strong>: <strong>normal</strong></p></td>
<td><p>Abra o formulário produtos.</p></td>
</tr>
<tr class="even">
<td><p><strong>SetValue</strong></p></td>
<td><p><strong>Item</strong>: [formulários]! [Produtos]! [CódigoDoFornecedor] <strong>Expressão</strong>: CódigoDoFornecedor</p></td>
<td><p>Defina o controle de ID do fornecedor como o fornecedor atual no formulário fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle de ID de categoria.</p></td>
</tr>
</tbody>
</table>


A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** . Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** . Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.

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
<td><p><strong>Echo ativado</strong>: <strong>não</strong></p></td>
<td><p>Interrompa a atualização da tela enquanto a macro estiver em execução.</p></td>
</tr>
<tr class="even">
<td><p>Énulo ([CódigoDoFornecedor])</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: mova para o registro de fornecedor cujos produtos você deseja ver e, em seguida, clique no botão revisar produtos novamente. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: selecionar um fornecedor</p></td>
<td><p>Se não houver um fornecedor atual no formulário fornecedores, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do controle</strong>: CompanyName</p></td>
<td><p>Mover o foco para o controle CompanyName.</p></td>
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
<td><p><strong>Nome do formulário</strong>: <strong>modo de exibição</strong>de lista de produtos: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [CódigoDoFornecedor] = [formulários]! [Fornecedores]! [CódigoDoFornecedor] <strong>Modo de dados</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>normal</strong></p></td>
<td><p>Abra o formulário lista de produtos e mostre os produtos do fornecedor atual.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>Moveredimensionarjanela</strong></p></td>
<td><p><strong>direita</strong>: 0,7799&quot; <strong>baixo</strong>: 1,8&quot;</p></td>
<td><p>Posicione o formulário lista de produtos no canto inferior direito do formulário fornecedores.</p></td>
</tr>
</tbody>
</table>

