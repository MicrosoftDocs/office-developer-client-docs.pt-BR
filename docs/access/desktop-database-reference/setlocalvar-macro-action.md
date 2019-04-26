---
title: 'Ação da macro SetLocalVar '
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314585"
---
# <a name="setlocalvar-macro-action"></a>Ação da macro SetLocalVar 

**Aplica-se ao**: Access 2013, Office 2013

Use a ação **DefinirVarLocal** para criar uma variável temporária e defini-la com um valor específico.

## <a name="setting"></a>Definição

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
<td><p>Uma expressão que será usada para definir o valor dessa variável temporária. Não preceda a expressão com o sinal de igualdade (=). Você pode clicar no botão <strong>Build</strong> para usar o <strong>Construtor de Expressões</strong> para definir esse argumento.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentários

As variáveis criadas pela ação **DefinirVarLocal** somente podem ser usadas na macro onde foram definidas. Use a ação **[DefinirVarLocal](settempvar-macro-action.md)** para definir uma variável que pode ser usada em outra macro, em um procedimento de evento ou em um formulário ou relatório.

Após a criação de uma variável temporária, você poderá fazer referência a ela em uma expressão. Por exemplo, se criar uma variável temporária com o nome MinhaVar, você poderá usá-la como fonte de controle de uma caixa de texto, usando esta sintaxe.

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> Em um Macro de dados, não é necessário usar o conjunto LocalVars para referir a uma variável. Por exemplo, se você criou uma variável temporária em uma Macro de dados chamada TotalAmount, você pode usar a variável como a fonte do controle para uma caixa de texto usando a seguinte sintaxe: `=[TotalAmount]`.

