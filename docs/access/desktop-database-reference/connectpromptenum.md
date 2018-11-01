---
title: ConnectPromptEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: ConnectPromptEnum
ms:assetid: 81dff685-b2e4-467e-75cc-b8c5bf80fb75
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249561(v=office.15)
ms:contentKeyID: 48545965
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 387e9a853a306b2375034359ce26db50685afcc4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887905"
---
# <a name="connectpromptenum"></a>ConnectPromptEnum

**Aplica-se a**: Access 2013, o Office 2013

Especifica se uma caixa de diálogo deve ser exibida para avisar sobre parâmetros ausentes ao abrir uma conexão para uma fonte de dados.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPromptAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Avisar sempre.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptComplete</strong></p></td>
<td><p>2</p></td>
<td><p>Avisar se mais informações forem necessárias.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPromptCompleteRequired</strong></p></td>
<td><p>3</p></td>
<td><p>Avisar se mais informações forem necessárias, mas se os parâmetros opcionais não forem permitidos.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPromptNever</strong></p></td>
<td><p>4</p></td>
<td><p>Nunca avisar.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ConnectPrompt.ALWAYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.COMPLETE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ConnectPrompt.COMPLETEREQUIRED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ConnectPrompt.NEVER</p></td>
</tr>
</tbody>
</table>

