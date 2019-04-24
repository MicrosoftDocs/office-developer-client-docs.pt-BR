---
title: CursorLocationEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295209"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Aplica-se ao:** Access 2013, Office 2013

Especifica o local do serviço do cursor.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adUseClient</strong></p></td>
<td><p>3D</p></td>
<td><p>Usa cursores do lado do cliente fornecidos por uma biblioteca de cursores local. Os serviços de cursores locais permitirão, com frequência, muitos recursos que os cursores fornecidos por drivers não permitirão, portanto, usar essa configuração poderá oferecer uma vantagem com relação aos recursos que estarão ativados. Para compatibilidade com versões anteriores, também há suporte para o sinônimo <strong>adUseClientBatch</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Não usa os serviços de cursor. (Essa constante é obsoleta e aparece somente para fins de compatibilidade com versões anteriores.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>duas</p></td>
<td><p>Padrão. Usa os cursores de provedores de dados ou fornecidos pelo driver. Esses cursores são, algumas vezes, muito flexíveis e permitem sensibilidade adicional para alterações que os outros fazem na fonte de dados. No enTanto, alguns recursos do <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">serviço de cursor da Microsoft para OLE DB</a> (como objetos <a href="recordset-object-ado.md">Recordset</a> desassociados) não podem ser simulados com cursores do lado do servidor e esses recursos não estarão disponíveis nessa configuração.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente do ADO/WFC

Pacote: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. CursorLocation. CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. CursorLocation. NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. CursorLocation. SERVER</p></td>
</tr>
</tbody>
</table>

