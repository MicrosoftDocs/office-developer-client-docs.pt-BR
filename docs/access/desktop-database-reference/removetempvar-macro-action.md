---
title: Ação da macro RemoverVariávelTemporária
TOCTitle: RemoveTempVar macro action
ms:assetid: 7bcc5010-3e30-ecef-2c5d-a35e73c8e325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196352(v=office.15)
ms:contentKeyID: 48545822
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm147125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5051cfd74f2a745ee430f2ed8a20445d2f9965f3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716303"
---
# <a name="removetempvar-macro-action"></a>Ação da macro RemoverVariávelTemporária


**Aplica-se a**: Access 2013, o Office 2013



Você pode usar a ação **RemoverVariávelTemporária** para remover uma única variável temporária criada usando a ação **DefinirVariávelTemporária**.

## <a name="setting"></a>Configuração

A ação **RemoverVariávelTemporária** tem os seguintes argumentos.

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
<td><p><strong>Name</strong></p></td>
<td><p>Insira o nome da variável temporária que deseja remover.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

  - É possível ter até 255 variáveis temporárias definidas de cada vez. Se você não remover uma variável temporária, ela permanecerá na memória até o banco de dados ser fechado. É recomendável remover as variáveis temporárias quando acabar de usá-las.

  - O Access remove automaticamente todas as variáveis temporárias ao fechar o banco de dados ou projeto.

  - Se você errar na grafia do nome da variável a ser removida, o Access não exibirá um erro. A variável que deveria ser removida permanecerá na memória até o banco de dados ser fechado.

  - Se você criou mais de uma variável temporária e deseja remover todas de uma só vez, use a ação **RemoverTodasVariáveisTemporárias**.

  - Para executar a ação **RemoverVariávelTemporária** em um módulo do VBA, use o método **Remove** do objeto **TempVars**.

## <a name="example"></a>Exemplo

A macro a seguir demonstra como criar uma variável temporária, usá-la em uma condição e uma caixa de mensagens e removê-la usando a ação **RemoverVariávelTemporária**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Condição</p></th>
<th><p>Ação</p></th>
<th><p>Argumentos</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Definirvariáveltemporária</strong></p></td>
<td><p><strong>Nome</strong>: MINHAVARIÁVEL<strong>expressão</strong>: CaixaDeEntrada (&quot;Insira um número diferente de zero.&quot;)</p></td>
</tr>
<tr class="even">
<td><p>[Varstemp]! [MINHAVARIÁVEL] &lt; &gt;0</p></td>
<td><p><strong>CaixaDeMensagem</strong></p></td>
<td><p><strong>Mensagem</strong>: =&quot;você digitou &quot; &amp; [Varstemp]! [MINHAVARIÁVEL] &amp; &quot;. &quot; <strong>Alarme sonoro</strong>: <strong>YesType</strong>: <strong>informações</strong></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><strong>Removervariáveltemporária</strong></p></td>
<td><p><strong>Nome</strong>: MinhaVar</p></td>
</tr>
</tbody>
</table>

