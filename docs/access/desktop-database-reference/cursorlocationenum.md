---
title: CursorLocationEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7f8eedd1245be16d87a2d3b2cd2b9121853529c5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863623"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Aplica-se a**: Access 2013 | Office 2013

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
<th><p>Constante</p></th>
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>Utiliza cursores do lado do cliente fornecidos por uma biblioteca de cursor local. Serviços do local do cursor frequentemente permitirá que muitos recursos fornecidos pelo driver cursores não podem, portanto o uso dessa configuração pode fornecer uma vantagem com relação a recursos que será habilitado. Para compatibilidade com versões anteriores, o sinônimo <strong>adUseClientBatch</strong> também é suportada.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Não usa os serviços de cursor. (Essa constante é obsoleta e aparece somente para fins de compatibilidade com versões anteriores.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Padrão. Usa o provedor de dados ou cursores fornecidos pelo driver. Esses cursores às vezes são muito flexíveis e permitem a sensibilidade adicional sobre as alterações que outras pessoas fazem à fonte de dados. No entanto, alguns recursos do <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service para OLE DB</a> (por exemplo, os objetos <a href="recordset-object-ado.md">Recordset</a> desassociados) não podem ser simulados com cursores do servidor e esses recursos estarão indisponíveis com essa configuração.</p></td>
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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

