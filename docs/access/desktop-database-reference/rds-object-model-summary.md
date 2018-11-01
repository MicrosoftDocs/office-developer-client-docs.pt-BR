---
title: Resumo de modelos de objeto RDS
TOCTitle: RDS Object Model Summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d15e451b99c54989e5168d99058cc4dd6ed79232
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875865"
---
# <a name="rds-object-model-summary"></a>Resumo de modelos de objeto RDS


**Aplica-se a**: Access 2013, o Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS. DataSpace</a></p></td>
<td><p>Este objeto contém um método para obter um servidor proxy. O proxy pode ser o programa de servidor padrão ou um programa de servidor personalizado (objeto corporativo). O programa de servidor pode ser chamado na Internet, em uma intranet, em uma rede local ou pode ser uma biblioteca de vínculo dinâmico local.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">Rdsserver</a></p></td>
<td><p>Este objeto representa o programa de servidor padrão. Ele executa o comportamento padrão de recuperação e atualização de dados RDS.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS. DataControl</a></p></td>
<td><p>Este objeto pode chamar automaticamente os objetos <strong>RDS.DataSpace</strong> e <strong>RDSServer.DataFactory</strong>.
 Utilize-o para chamar o comportamento padrão de recuperação ou atualização de dados RDS. Este objeto também permite que controles visuais acessem o objeto <strong>Recordset</strong> retornado.</p></td>
</tr>
</tbody>
</table>

