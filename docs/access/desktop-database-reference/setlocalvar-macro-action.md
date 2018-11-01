---
title: Ação de macro DefinirVarLocal
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 299227553481c4f149827c31078111db7b427f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886638"
---
# <a name="setlocalvar-macro-action"></a>Ação de macro DefinirVarLocal


**Aplica-se a**: Access 2013, o Office 2013

Use a ação **DefinirVarLocal** para criar uma variável temporária e defini-la com um valor específico.

## <a name="setting"></a>Configuração

A ação **DefinirVarLocal** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nome</strong></p></td>
<td><p>Sim</p></td>
<td><p>Uma cadeia de caracteres que especifica o nome da variável.</p></td>
</tr>
<tr class="even">
<td><p><strong>Expressão</strong>.</p></td>
<td><p>Sim</p></td>
<td><p>Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igual (=). Você pode clicar no botão <strong>Construir</strong> para usar o <strong>Construtor de expressões</strong> para definir este argumento.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

As variáveis criadas pela ação **DefinirVarLocal** somente podem ser usadas na macro onde foram definidas. Use a ação **[DefinirVarLocal](settempvar-macro-action.md)** para definir uma variável que pode ser usada em outra macro, em um procedimento de evento ou em um formulário ou relatório.

Após a criação de uma variável temporária, você poderá fazer referência a ela em uma expressão. Por exemplo, se criar uma variável temporária com o nome MinhaVar, você poderá usá-la como fonte de controle de uma caixa de texto, usando esta sintaxe.

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P>[!OBSERVAçãO] Em uma Macro de Dados, não é necessário usar a coleção LocalVars para fazer referência a uma variável. Por exemplo, se você criou uma variável temporária em uma Macro de dados denominado TotalAmount, você pode usar a variável como a fonte de controle para uma caixa de texto usando a seguinte sintaxe<BR>= [TotalAmount]</P>


