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

Você pode usar a ação **MessageBox** para exibir uma caixa de mensagem contendo um aviso ou uma mensagem informativa. Por exemplo, você pode usar a ação **MessageBox** com macros de validação. Quando um controle ou registro falha em uma condição de validação na macro, uma caixa de mensagem pode exibir uma mensagem de erro e fornecer instruções sobre o tipo de dados que devem ser inseridos.

## <a name="setting"></a>Configuração

A ação **MessageBox** tem os seguintes argumentos.

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
<td><p>O texto na caixa de mensagem. Insira o texto da mensagem na caixa <strong>mensagem</strong> na seção <strong>argumentos da ação</strong> do painel Construtor de macros. Você pode digitar até 255 caracteres ou inserir uma expressão (precedida por um sinal de igual).</p></td>
</tr>
<tr class="even">
<td><p><strong>Beep</strong></p></td>
<td><p>Especifica se o alto-falante do computador emite um sinal sonoro quando a mensagem é exibida. Clique em <strong>Sim</strong> (soar o sinal sonoro) ou <strong>não</strong> (não emitir o sinal sonoro). O padrão é <strong>Sim</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Tipo</strong></p></td>
<td><p>O tipo de caixa de mensagem. Cada tipo tem um ícone diferente. Clique em <strong>nenhum</strong>, <strong>crítico</strong>, <strong>aviso?</strong>, <strong>aviso!</strong>ou <strong>informações</strong>. O padrão é <strong>nenhum</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Title</strong></p></td>
<td><p>O texto exibido na barra de título da caixa de mensagem. Por exemplo, você pode fazer com que a barra &quot;de título exiba&quot;a validação da ID do cliente. Se você deixar este argumento em branco &quot;, o&quot; Microsoft Access será exibido.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Você pode usar a ação **MessageBox** para criar uma mensagem de erro formatada semelhante às mensagens de erro internas exibidas pelo Microsoft Access. A ação **MessageBox** permite que você forneça uma mensagem em três seções para o argumento da mensagem. Separe as seções com o caractere "@".

O exemplo a seguir exibe uma caixa de mensagem formatada com uma mensagem com seção. A primeira seção de texto na mensagem é exibida como um título em negrito. A segunda seção é exibida como texto sem formatação abaixo desse título. A terceira seção é exibida como texto sem formatação abaixo da segunda seção, com uma linha em branco entre elas.

Digite a seguinte cadeia de caracteres no argumento **Message** :

**Botão\!incorreto @This botão não funciona. @Try outro.**

Você não pode executar a ação **MessageBox** em um módulo do VBA (Visual Basic for Applications). Em vez disso, use a função **MsgBox** .

## <a name="examples"></a>Exemplos

**Sincronizar formulários usando uma macro**

A macro a seguir abre um formulário de lista de produtos no canto inferior direito do formulário fornecedores, exibindo os produtos do fornecedor atual. Ela mostra o uso das ações **eco**, **MessageBox**, **IrParaControle**, **PararMacro**, **AbrirFormulário**e **moveredimensionarjanela** . Também mostra o uso de uma expressão condicional com as ações **MessageBox**, **IrParaControle**e **PararMacro** . Essa macro deve ser anexada ao botão reVisar produtos no formulário fornecedores.

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


**Validar dados usando uma macro**

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato correto para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. Em seguida, ele retorna ao controle PostalCode, onde você pode corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>IsNull ([CountryRegion])</p></td>
<td><p><strong>PararMacro</strong></p></td>
<td><p></p></td>
<td><p>Se CountryRegion for <strong>nulo</strong>, o código postal não poderá ser validado.</p></td>
</tr>
<tr class="even">
<td><p>CountryRegion In (&quot;França&quot;,&quot;Itália&quot;,&quot;Espanha&quot;) e compr ([CEP] &lt; &gt; ) 5</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: o código postal deve ter 5 caracteres. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
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
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>CountryRegion In (&quot;Austrália&quot;,&quot;Cingapura&quot;) e compr ([CEP] &lt; &gt; ) 4</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: o código postal deve ter quatro caracteres. <strong>Aviso sonoro</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
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
<td><p><strong>Nome do controle</strong>: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot;Canadá&quot;) E ([CEP] não like&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;)</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: o código postal não é válido. Exemplo de código canadense: H1J 1C3 <strong>beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erro de código postal</p></td>
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

