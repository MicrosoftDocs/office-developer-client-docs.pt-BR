---
title: Ação da macro CaixaDeMensagem
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1175e3903e54fd3420be43dfd9e3652d9990468b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289153"
---
# <a name="messagebox-macro-action"></a>Ação da macro CaixaDeMensagem

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a **ação MessageBox** para exibir uma caixa de mensagem contendo um aviso ou uma mensagem informativa. Por exemplo, você pode usar a **ação MessageBox** com macros de validação. Quando um controle ou registro falha em uma condição de validação na macro, uma caixa de mensagem pode exibir uma mensagem de erro e fornecer instruções sobre o tipo de dados que devem ser inseridos.

## <a name="setting"></a>Setting

A **ação MessageBox** tem os seguintes argumentos.

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
<td><p><strong>Message</strong></p></td>
<td><p>O texto na caixa de mensagem. Insira o texto da mensagem <strong>na caixa Mensagem</strong> na seção <strong>Argumentos da</strong> Ação do painel Construtor de Macros. Você pode digitar até 255 caracteres ou inserir uma expressão (precedida por um sinal de igual).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Especifica se o alto-falante do computador emitirá um tom de alarme sonoro quando a mensagem for exibida. Clique <strong>em Sim</strong> (soe o tom de alarme sonoro) ou <strong>Não</strong> (não soe o tom de alarme sonoro). O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo</strong></p></td>
<td><p>O tipo de caixa de mensagem. Cada tipo tem um ícone diferente. Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>. O padrão é <strong>Nenhum</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>O texto exibido na barra de título da caixa de mensagem. Por exemplo, você pode fazer a barra de título exibir &quot; a Validação de ID do &quot; Cliente. Se você deixar esse argumento em branco, &quot; o Microsoft Access será &quot; exibido.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar a **ação MessageBox** para criar uma mensagem de erro formatada semelhante às mensagens de erro integradas exibidas pelo Microsoft Access. A **ação MessageBox** permite que você fornece uma mensagem em três seções para o argumento Message. Separe as seções com o caractere "@".

O exemplo a seguir exibe uma caixa de mensagem formatada com uma mensagem seçãoda. A primeira seção do texto da mensagem é exibida como um título em negrito. A segunda seção é exibida como texto sem texto simples abaixo desse título. A terceira seção é exibida como texto sem texto simples abaixo da segunda seção, com uma linha em branco entre elas.

Digite a seguinte cadeia de caracteres no **argumento Message:**

**Botão \! errado @This botão não work.@Try outro.**

Não é possível executar a **ação MessageBox** em um módulo do VBA (Visual Basic for Applications). Use a **função MsgBox** em vez disso.

## <a name="examples"></a>Exemplos

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de Lista de Produtos no canto inferior direito do formulário Fornecedores, exibindo os produtos do fornecedor atual. Ele mostra o uso das ações **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm** e **MoveAndSizeWindow.** Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl** e **StopMacro.** Essa macro deve ser anexada ao botão Revisar Produtos no formulário Fornecedores.

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


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato correto para o país/região, a macro exibirá uma caixa de mensagem e cancelará o gravação do registro. Em seguida, ele retorna você para o controle postalCode, onde você pode corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>[CountryRegion] In ( &quot; França , Itália , Espanha ) e &quot; &quot; &quot; &quot; &quot; Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>o código postal deve ter 5 caracteres. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não tiver 5 caracteres, exiba uma mensagem.</p></td>
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
<td><p>[CountryRegion] In ( &quot; Austrália &quot; , &quot; &quot; Cingapura ) e Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>o código postal deve ter 4 caracteres. <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não tiver 4 caracteres, exiba uma mensagem.</p></td>
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
<td><p>([CountryRegion] = &quot; Canadá &quot; ) e ([PostalCode] não como &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem:</strong>O código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</p></td>
<td><p>Se o código postal não estiver correto para Canadá, exiba uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p><strong>CancelEvent</strong></p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
</tbody>
</table>

