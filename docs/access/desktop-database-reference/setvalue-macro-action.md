---
title: Ação da macro DefinirValor
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1ec96fd588e4b20b6c2ebe0ef25f488841aa4d70
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998872"
---
# <a name="setvalue-macro-action"></a>Ação da macro DefinirValor

**Aplica-se a**: Access 2013, o Office 2013

Você pode usar a ação **DefinirValor** para definir o valor de um campo do Microsoft Access, o controle ou a propriedade em um formulário, uma folha de dados do formulário ou um relatório.

> [!NOTE]
> - Você não pode usar a ação **DefinirValor** para definir o valor de uma propriedade que retorna um objeto do Access.
> - [!OBSERVAçãO] This action will not be allowed if the database is not trusted. 

## <a name="setting"></a>Configuração

A ação **DefinirValor** tem os seguintes argumentos.

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
<td><p><strong>1.1</strong></p></td>
<td><p>O nome do campo, controle ou a propriedade cujo valor você deseja definir. Insira o nome de campo, controle ou propriedade na caixa de <strong>Item</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. Você deve usar a sintaxe completa para se referir a este item, como <em>controlname</em> (para um controle no formulário ou relatório do qual a macro foi chamada) ou <strong>formulários</strong>! <em>formname</em>! <em>controlname</em>. Este é um argumento obrigatório.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expressão</strong>.</p></td>
<td><p>A expressão que Access usa para definir o valor deste item. Você sempre deve usar a sintaxe completa para se referir a quaisquer objetos na expressão. Por exemplo, para aumentar o valor em um controle salário em um formulário Employees em 10 por cento, use Forms! Funcionários! Salário * 1.1. Este é um argumento obrigatório.</p><p><strong>Observação</strong>: você não deve usar um sinal de igual (=) antes da expressão neste argumento. Se fizer isso, o Access avalia a expressão e, em seguida, usa esse valor como a expressão neste argumento. Isso pode gerar resultados inesperados se a expressão for uma cadeia de caracteres.</p>
<p>Por exemplo, se você digitar <strong> = &quot;sequência1&quot; </strong> para este argumento, o Access primeiro avalia a expressão como Sequência1. Em seguida, ele usa String1 como a expressão neste argumento, esperando encontrar um controle ou a propriedade chamada String1 no formulário ou relatório que chamou a macro.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Em um banco de dados do Access (. mdb ou. accdb), clique no botão **Construir** para usar o construtor de expressões para criar uma expressão para um desses argumentos.

## <a name="remarks"></a>Comentários

Você pode usar esta ação para definir um valor para um campo ou controle em um formulário, uma folha de dados do formulário ou um relatório. Você também pode definir o valor para quase todas as propriedades do relatório, formulário e controle em qualquer modo. Para descobrir se uma determinada propriedade pode ser definida usando uma macro e quais modos de exibição pode ser definida, consulte o tópico de ajuda para essa propriedade no Editor do Visual Basic.

Você também pode definir o valor de um campo na tabela de base de um formulário, mesmo se o formulário não contiver um controle acoplado ao campo. Use a sintaxe **formulários**\!*formname*\!*fieldname* na caixa de **Item** para definir o valor desse campo. Você também pode consultar a um campo da tabela base de um relatório usando a sintaxe **relatórios**\!*reportname*\!*fieldname*, mas deve haver um controle no relatório acoplado a esse campo ou o campo deve ser referido em um controle calculado no relatório.

Se você definir o valor de um controle em um formulário, a ação **DefinirValor** não aciona as regras de validação de nível de formulário do controle, mas ela acionará as regras de validação de nível de tabela do campo base se o controle é um controle acoplado. A ação **DefinirValor** também aciona o recálculo, mas o recálculo pode não acontecer imediatamente. Para acionar um redesenho imediato e forçar a conclusão do recálculo, use a ação **RedesenharObjeto** . O valor definido em um controle usando a ação **DefinirValor** também não é afetado por uma máscara de entrada definida do controle ou propriedade de **máscara de entrada** do campo de base.

Para alterar o valor de um controle, você pode usar a ação **DefinirValor** em uma macro especificada pela propriedade de evento **AfterUpdate** do controle. No entanto, você não pode usar a ação **DefinirValor** em uma macro especificada pela propriedade de evento **BeforeUpdate** de um controle para alterar o valor do controle (embora você pode usar a ação **DefinirValor** para alterar o valor de outros controles). Você também pode usar a ação **DefinirValor** em uma macro especificada pela propriedade **BeforeUpdate** ou **AfterUpdate** de um formulário para alterar o valor de quaisquer controles no registro atual.

> [!NOTE]
> Você não pode usar a ação **DefinirValor** para definir o valor dos controles a seguir:
> - Controles vinculados e controles calculados em relatórios.
> - Controles calculados em formulários.

> [!TIP]
> Você pode usar a ação **DefinirValor** para ocultar ou mostrar um formulário no modo formulário. Insira **Forms**! *formname * * *. Visível** na caixa de **Item** e **não** ou **Sim** na caixa **expressão** . A definição da propriedade **visível** do formulário uma janela restrita como **não** oculta o formulário e o torna sem janela restrita. Configuração da propriedade como **Sim** exibe o formulário e o torna restrito novamente.

Alterando o valor da ou adicionando novos dados em um controle usando a ação **DefinirValor** em uma macro não aciona eventos como **BeforeUpdate**, **BeforeInsert**ou **Change** que ocorrem quando você altera ou insere dados nesses controles através do interface do usuário. Esses eventos também não ocorrem se você definir o valor do controle usando um Visual Basic para módulo Applications (VBA).

Esta ação não está disponível em um módulo do VBA. Defina o valor diretamente no VBA.

## <a name="example"></a>Exemplo

**Definir o valor de um controle usando uma macro**

A macro a seguir abre o formulário Adicionar produtos com um botão no formulário Suppliers. Ela mostra o uso do **eco**, **fecharJanela**, **AbrirFormulário**, **DefinirValor**e **GoToControl** ações. A ação **DefinirValor** define o controle de SupplierID no formulário produtos como o fornecedor atual no formulário fornecedores. A ação **GoToControl** , em seguida, move o foco para o campo CategoryID, onde você pode começar a inserir dados para o novo produto. Essa macro deve ser anexada ao botão Adicionar produtos no formulário fornecedores.

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
<td><p>Defina o controle de SupplierID como o fornecedor atual no formulário fornecedores.</p></td>
</tr>
<tr class="odd">
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: CategoryID</p></td>
<td><p>Vá para o controle CategoryID.</p></td>
</tr>
</tbody>
</table>

