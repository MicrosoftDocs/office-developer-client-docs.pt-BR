---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bd8196670513156011d69f08eacf790fa4a0a03
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703150"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Aplica-se a**: Access 2013, o Office 2013

Especifica o comportamento do objeto [Record](record-object-ado.md) do método [MoveRecord](moverecord-method-ado.md).

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
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Padrão. Executa a operação mover padrão: A operação falha se o arquivo ou diretório de destino já existir e a operação atualizar links de hipertexto.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Sobregrava o arquivo ou diretório de destino, mesmo se ele já existir.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Modifica o comportamento padrão do método <strong>MoveRecord</strong> por não atualizar os links de hipertexto do <strong>Record</strong> de origem. O comportamento padrão depende dos recursos do provedor. A operação mover atualiza os links se o provedor tiver recursos. Se ele não puder consertar os links ou se este valor não for especificado, a operação mover terá êxito mesmo que os links não sejam consertados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Solicita que o provedor tente simular a operação mover (usando as operações download, upload e excluir). Se a tentativa de mover o <strong>Record</strong> falhar porque o URL de destino está em um servidor diferente ou está sendo atendido por um provedor diferente da origem, isso poderá causar um aumento na latência ou a perda de dados, devido aos recursos diferentes do provedor ao mover os recursos entre os provedores.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Equivalente ADO/WFC

Essas constantes não têm ADO/WFC equivalentes.

