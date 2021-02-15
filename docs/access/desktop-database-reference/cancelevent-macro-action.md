---
title: Ação da macro CancelarEvento
TOCTitle: CancelEvent macro action
ms:assetid: d9d3ea99-c9fb-2524-c570-e3ee6d20af98
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835110(v=office.15)
ms:contentKeyID: 48548066
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm78430
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b55fc51f70bcc2c9d2f7e93cf9c79228cd2fe440
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296630"
---
# <a name="cancelevent-macro-action"></a>Ação da macro CancelarEvento

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a **ação CancelarEvento** para cancelar o evento que fez o Access executar a macro que contém essa ação. O nome da macro é a configuração de uma propriedade de evento como **AntesDeAtualizar**, **AoAbrir**, **OnUnload** ou **OnPrint**.

## <a name="setting"></a>Setting

A ação **CancelarEvento** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Em um formulário, normalmente é usada a ação **CancelarEvento** em uma macro de validação com a propriedade de evento **AntesDeAtualizar**. Quando um usuário insere dados em um controle ou registro, o Access executa a macro antes de adicioná-los ao banco de dados. Se os dados falharem nas condições de validação da macro, a ação **CancelarEvento** cancelará o processo de atualização antes de ser iniciado.

Geralmente, você usa esta ação com a ação **CaixadeMensagem** para indicar que os dados falharam nas condições de validação e para fornecer informações úteis sobre o tipo de dados que deve ser inserido.

Os eventos a seguir podem ser cancelados pala ação **CancelarEvento**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>ApplyFilter</strong></p></td>
<td><p><strong>Dirty</strong></p></td>
<td><p><strong>MouseDown</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeDelConfirm</strong></p></td>
<td><p><strong>Exit</strong></p></td>
<td><p><strong>NoData</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>BeforeInsert</strong></p></td>
<td><p><strong>Filtro</strong></p></td>
<td><p><strong>Open</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>BeforeUpdate</strong></p></td>
<td><p><strong>Formato</strong></p></td>
<td><p><strong>Print</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>DblClick</strong></p></td>
<td><p><strong>KeyPress</strong></p></td>
<td><p><strong>Unload</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Delete</strong></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Você pode usar a ação **CancelarEvento** com o evento **PressionarMouse** somente para cancelar o evento que ocorre ao clicar com o botão direito do mouse em um objeto.

Se a configuração da propriedade de evento **OnDblClick** de um controle especificar uma macro que contém a ação **CancelarEvento**, esta cancelará o evento **ClicarDuasVezes**.

Para eventos que podem ser cancelados, o comportamento padrão do evento (ou seja, o que o Access normalmente faz na ocorrência do evento) ocorre após a execução da macro do evento. Isso permite cancelar o comportamento padrão. Por exemplo, quando você clica duas vezes em uma palavra sobre a qual está o ponto de inserção em uma caixa de texto, o Access normalmente seleciona a palavra. É possível cancelar esse comportamento padrão na macro do evento **ClicarDuasVezes** e executar alguma outra ação, como abrir um formulário que contém informações sobre os dados na caixa de texto. Para eventos que não podem ser cancelados, o comportamento padrão ocorre antes de a macro ser executada.

> [!NOTE]
> [!OBSERVAçãO] Se a propriedade de evento **OnUnload** de um formulário especificar uma macro que executa uma ação **CancelarEvento**, você não conseguirá fechar o formulário. Será necessário corrigir a condição que causou a execução da ação **CancelarEvento** ou abrir a macro e excluir a ação **CancelarEvento**. Se o formulário for restrito, você não conseguirá abrir a macro.

Para executar a ação **CancelarEvento** em um módulo do VBA (Visual Basic for Applications), use o método **CancelEvent** do objeto **DoCmd**.

## <a name="example"></a>Exemplo

Validar dados usando uma macro

A macro de validação a seguir verifica os códigos postais inseridos em um formulário Fornecedores. Ela mostra o uso das ações **PararMacro**, **CaixadeMensagem**, **CancelarEvento** e **IrParaControle**. Uma expressão condicional verifica o país/região e o código postal inseridos em um registro do formulário. Se o código postal não estiver no formato certo para o país/região, a macro exibirá uma caixa de mensagem e cancelará o salvamento do registro. Ela retornará o controle de Código Postal, em que será possível corrigir o erro. Essa macro deve ser anexada à propriedade **AntesdeAtualizar** do formulário Fornecedores.

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
<td><p>PararMacro</p></td>
<td><p></p></td>
<td><p>Se PaísRegião for <strong>Nulo</strong>, o código postal não poderá ser validado.</p></td>
</tr>
<tr class="even">
<td><p>[CountryRegion] In ( &quot; França , Itália , Espanha ) e &quot; &quot; &quot; &quot; &quot; Len([CEP]) &lt; &gt; 5</p></td>
<td><p>CaixaDeMensagem</p></td>
<td><p>Mensagem: O código postal precisa ter 5 caracteres. Alarme sonoro: <strong>Sim</strong> Tipo: <strong>Título da</strong> Informação: Erro de Código Postal</p></td>
<td><p>Se o código postal não tiver 5 caracteres, exiba uma mensagem.</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nome do Controle: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>[CountryRegion] In ( &quot; Austrália &quot; , &quot; &quot; Cingapura ) e Len([CEP]) &lt; &gt; 4</p></td>
<td><p>CaixaDeMensagem</p></td>
<td><p>Mensagem: O código postal precisa ter 4 caracteres. Alarme sonoro: <strong>Sim</strong> Tipo: <strong>Título da</strong> Informação: Erro de Código Postal</p></td>
<td><p>Se o código postal não tiver 4 caracteres, exiba uma mensagem.</p></td>
</tr>
<tr class="even">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p>GoToControl</p></td>
<td><p>Nome do Controle: CEP</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>([CountryRegion] = &quot; Canadá &quot; ) e ([cep] não como &quot; [A-Z][0-9][A-Z] [0-9][A-Z][0-9] &quot; )</p></td>
<td><p>CaixaDeMensagem</p></td>
<td><p>Mensagem: O código postal é inválido. Exemplo de código canadense: H1J 1C3 Beep: <strong>Yes</strong> Type: <strong>Information</strong> Title: Postal Code Error</p></td>
<td><p>Se o código postal não estiver correto para Canadá, exiba uma mensagem. (Exemplo de código de Canadá: H1J 1C3)</p></td>
</tr>
<tr class="odd">
<td><p>...</p></td>
<td><p>CancelEvent</p></td>
<td><p></p></td>
<td><p>Cancele o evento.</p></td>
</tr>
</tbody>
</table>

