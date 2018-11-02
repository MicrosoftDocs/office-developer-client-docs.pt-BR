---
title: Ação da macro CaixaDeMensagem
TOCTitle: MessageBox macro action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f501b5884a8149850df7c1d16a141f345da90e52
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925426"
---
# <a name="messagebox-macro-action"></a>Ação da macro CaixaDeMensagem


**Aplica-se a**: Access 2013, o Office 2013




Você pode usar a ação **MessageBox** para exibir uma caixa de mensagem contendo um aviso ou uma mensagem informativa. Por exemplo, você pode usar a ação **MessageBox** com macros de validação. Quando um controle ou registro falha uma condição de validação na macro, uma caixa de mensagem pode exibir uma mensagem de erro e forneça instruções sobre o tipo de dados que devem ser inseridos.

## <a name="setting"></a>Configuração

A ação de **MessageBox** tem os seguintes argumentos.

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
<td><p><strong>Mensagem</strong></p></td>
<td><p>O texto na caixa de mensagem. Insira o texto da mensagem na caixa de <strong>mensagem</strong> na seção <strong>Argumentos da ação</strong> do painel de tarefas do construtor de macros. Você pode digitar até 255 caracteres ou inserir uma expressão (precedida por um sinal de igualdade).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Especifica se o alto-falante do seu computador emitirá um aviso sonoro quando a mensagem é exibida. Clique em <strong>Sim</strong> (som o aviso sonoro) ou <strong>não</strong> (não SOA o aviso sonoro). O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo</strong></p></td>
<td><p>O tipo de caixa de mensagem. Cada tipo tem um ícone diferente. Clique em <strong>Nenhum</strong>, <strong>crítico</strong>, <strong>Aviso?</strong>, <strong>Aviso!</strong>, ou <strong>informações</strong>. O padrão é <strong>None</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Título</strong></p></td>
<td><p>O texto exibido na barra de título da caixa de mensagem. Por exemplo, você pode ter a exibição da barra de título &quot;validação de ID de cliente&quot;. Se você deixar este argumento em branco, &quot;Microsoft Access&quot; é exibida.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar a ação **MessageBox** para criar uma mensagem de erro formatada semelhante às mensagens de erro internas exibidas pelo Microsoft Access. A ação **MessageBox** permite fornecer uma mensagem em três seções para o argumento de mensagem. Separa as seções com o "@" caractere.

O exemplo a seguir exibe uma caixa de mensagem formatada com uma mensagem dividida em seções. A primeira seção do texto da mensagem é exibida como um cabeçalho em negrito. A segunda seção é exibida como texto sem formatação abaixo do título. A terceira seção é exibida como texto simples abaixo da segunda seção, com uma linha em branco entre elas.

Digite a cadeia de caracteres a seguir no argumento **mensagem** :

**Botão errado\!@This botão não Work.@Try outro.**

Você não pode executar a ação de **MessageBox** em um módulo Visual Basic for Applications (VBA). Use a função **MsgBox** .

## <a name="examples"></a>Exemplos

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso do **eco**, **MessageBox**, **GoToControl**, **PararMacro**, **AbrirFormulário**e **Moveredimensionarjanela** ações. Ele também mostra o uso de uma expressão condicional com as ações **MessageBox**, **GoToControl**e **PararMacro** . Essa macro deve ser anexada ao botão Revisar produtos no formulário fornecedores.

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


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato correto para o país/região, a macro exibe uma caixa de mensagem e cancela o registro é salvo. Ele então retorna você ao controle PostalCode, onde é possível corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>IsNull([CountryRegion])</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Se CountryRegion for <strong>Nulo</strong>, o código postal não pode ser validado.</p></td>
</tr>
<tr class="even">
<td><p>[Paísregião] No (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e Len([PostalCode]) &lt; &gt; 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: O código postal precisa ter 5 caracteres. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</p></td>
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
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[Paísregião] No (&quot;Austrália&quot;,&quot;Cingapura&quot;) e Len([PostalCode]) &lt; &gt; 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: O código postal precisa ter 4 caracteres. <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de CEP</p></td>
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
<td><p><strong>IrParaControle</strong></p></td>
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([Paísregião] = &quot;Canadá&quot;) E ([CEP] não igual a&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: O código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>alarme sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código Postal</p></td>
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

