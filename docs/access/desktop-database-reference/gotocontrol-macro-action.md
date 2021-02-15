---
title: Ação da macro IrParaControle
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292164"
---
# <a name="gotocontrol-macro-action"></a>Ação da macro IrParaControle

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **GoToControl** para mover o foco para o campo ou controle especificado no registro atual do formulário aberto, folha de dados do formulário, folha de dados de tabela ou folha de dados de consulta. Use esta ação quando quiser que um campo ou controle específico tenha o foco. Esse campo ou controle pode ser usado para comparações ou **ações FindRecord.** Você também pode usar esta ação para navegar em um formulário de acordo com certas condições. Por exemplo, se o usuário inserir Não em um controle Casado de um formulário de seguro de saúde, o foco automaticamente poderá ignorar o controle Nome do cônjuge/parceiro e passar para o próximo controle.

## <a name="setting"></a>Setting

> [!NOTE]
> Essa ação não está disponível para uso com páginas de acesso a dados.

A ação **IrParaControle** tem os argumentos a seguir.

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
<td><p><strong>Nome do Controle</strong></p></td>
<td><p>O nome do campo ou do controle em que você deseja focar. Insira o nome do campo ou controle na caixa <strong>Nome do</strong> Controle na seção <strong>Argumentos</strong> da Ação do painel Construtor de Macros. Este é um argumento obrigatório.</p>
<p><strong>OBSERVAÇÃO:</strong>insira apenas o nome do campo ou controle no argumento <strong>Nome</strong> do Controle, não o identificador totalmente qualificado, como Formulários! Produtos! [ID do Produto].</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você não pode usar a **ação IrParaControle** para mover o foco para um controle em um formulário oculto.

> [!TIP]
> Você pode usar a **ação IrParaControle** para mover para um subform que é um tipo de controle. Em seguida, você pode usar **a ação IrParaRegiscord** para mover para um registro específico no subform que. Você também pode mover para um controle em um subform que usa a ação **IrParaControle** para mover primeiro para o subformform que, em seguida, para o controle no subformform.

Para executar a **ação GoToControl** em um módulo do VBA (Visual Basic for Applications), use o **método GoToControl** do objeto **DoCmd.** You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.

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
<td><p>Feche o formulário lista de produtos.</p></td>
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


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. Em seguida, a macro retorna você para o controle do Código Postal, onde você pode corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Se CountryRegion for <strong>Null</strong>, o código postal não poderá ser validado.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; França , Itália , Espanha ) e &quot; &quot; &quot; &quot; &quot; Len([CEP]) &lt; &gt; 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>o código postal deve ter 5 caracteres. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não tiver 5 caracteres, exibe uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do Controle</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Austrália &quot; , &quot; &quot; Cingapura ) e Len([CEP]) &lt; &gt; 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p>Mensagem: O código postal precisa ter 4 caracteres. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não tiver 4 caracteres, exibe uma mensagem.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>GoToControl</strong></p></td>
<td><p><strong>Nome do Controle</strong>: PostalCode</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canadá &quot; ) e ([cep] não como &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>O código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não estiver correto para o Canadá, exibe uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
</tbody>
</table>

