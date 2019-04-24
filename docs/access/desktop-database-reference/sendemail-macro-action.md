---
title: Ação da macro EnviarEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314648"
---
# <a name="sendemail-macro-action"></a>Ação da macro EnviarEmail

**Aplica-se ao:** Access 2013, Office 2013

A ação **EnviarEmail** envia uma mensagem de email.

> [!NOTE]
> A ação **EnviarEmail** está disponível somente em Macros de Dados.

## <a name="setting"></a>Configuração

A ação **EnviarEmail** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>To</strong></p></td>
<td><p>Sim</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>para</strong> da mensagem. Separe os nomes de destinatários especificados neste argumento (e nos argumentos <em>CC</em> e <em>Cco</em> ) com ponto e vírgula (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Não</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na linha CC (&quot;cópia&quot;carbono) na mensagem.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Não</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na linha Cco (&quot;com cópia&quot;oculta) da mensagem.</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject</strong></p></td>
<td><p>Não</p></td>
<td><p>O assunto da mensagem. Esse texto aparece na linha <strong>Assunto</strong> da mensagem de email.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Body</strong></p></td>
<td><p>Não</p></td>
<td><p>O texto que você deseja incluir no corpo principal da mensagem de email. Se você deixar esse argumento em branco, nenhum texto adicional será incluído na mensagem.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

A ação **EnviarEmail** está disponível somente nos eventos de macro **[Após Exclusão](after-delete-macro-event.md)**, **[Após Inserir](after-insert-macro-event.md)** e **[Após Atualizar](after-update-macro-event.md)**.

A ação **EnviarEmail** não exibe a mensagem para edição.

