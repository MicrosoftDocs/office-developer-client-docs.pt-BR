---
title: Ação da macro RemoverTodasVariáveisTemporárias
TOCTitle: RemoveAllTempVars macro action
ms:assetid: 409fd836-4a53-cefd-4264-8cee0fa8ac52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192877(v=office.15)
ms:contentKeyID: 48544430
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117413
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: eade809a6e3982dc0dc4cf94ae382af72e8f454e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306794"
---
# <a name="removealltempvars-macro-action"></a>Ação da macro RemoverTodasVariáveisTemporárias


**Aplica-se ao:** Access 2013, Office 2013


Você pode usar a ação **RemoverTodasVariáveisTemporárias** para remover todas as variáveis temporárias criadas usando a ação **DefinirVariávelTemporária**.

## <a name="setting"></a>Setting

A ação **RemoverTodasVariáveisTemporárias** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

  - É possível ter até 255 variáveis temporárias definidas de cada vez. Se você não remover uma variável temporária, ela permanecerá na memória até o banco de dados ou projeto ser fechado. É recomendável remover as variáveis temporárias quando acabar de usá-las.

  - O Access remove automaticamente todas as variáveis temporárias ao fechar o banco de dados ou projeto.

  - Para remover uma única variável temporária, use a ação **RemoverVariávelTemporária** e defina seu argumento com o nome da variável temporária que deseja remover.

  - Para executar a ação **RemoverTodasVariáveisTemporárias** em um módulo do VBA, use o método **RemoveAll** do objeto **TempVars**.

## <a name="example"></a>Exemplo

A macro a seguir demonstra como criar uma variável temporária, usá-la em uma condição e uma caixa de mensagens e removê-la usando a ação **RemoverTodasVariáveisTemporárias**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condition</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>SetTempVar</strong></p></td>
<td><p><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</p></td>
</tr>
<tr class="even">
<td><p>[TempVars]! [MyVar] &lt; &gt; 0</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: = &quot; Você entrou &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>RemoveAllTempVars</strong></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

