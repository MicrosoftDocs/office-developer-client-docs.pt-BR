---
title: Ação da macro EnviarEmail
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5016500b62a465f21ecab93a6fb66c9e6d514e1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998837"
---
# <a name="sendemail-macro-action"></a>Ação da macro EnviarEmail

**Aplica-se a**: Access 2013, o Office 2013

A ação **EnviarEmail** envia uma mensagem de email.

> [!NOTE]
> [!OBSERVAçãO] A ação **EnviarEmail** está disponível somente em Macros de Dados.

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
<th><p>Argumento</p></th>
<th><p>Obrigatório</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>To</strong></p></td>
<td><p>Sim</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na linha <strong>para</strong> da mensagem. Separe os nomes dos destinatários especificados neste argumento (e nos argumentos <em>Cc</em> e <em>Cco</em> ) com um ponto e vírgula (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Não</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na Cc (&quot;cópia carbono&quot;) linha da mensagem.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cco</strong></p></td>
<td><p>Não</p></td>
<td><p>Os destinatários da mensagem cujos nomes você deseja colocar na Cco (&quot;cópia oculta&quot;) linha da mensagem.</p></td>
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

