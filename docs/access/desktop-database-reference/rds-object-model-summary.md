---
title: Resumo de modelos de objeto RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300872"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="5dd60-102">Resumo de modelos de objeto RDS</span><span class="sxs-lookup"><span data-stu-id="5dd60-102">RDS object model summary</span></span>


<span data-ttu-id="5dd60-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5dd60-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5dd60-104">Objeto</span><span class="sxs-lookup"><span data-stu-id="5dd60-104">Object</span></span></p></th>
<th><p><span data-ttu-id="5dd60-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5dd60-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5dd60-106"><a href="dataspace-object-rds.md">RDS. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="5dd60-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="5dd60-p101">Este objeto contém um método para obter um servidor proxy. O proxy pode ser o programa de servidor padrão ou um programa de servidor personalizado (objeto corporativo). O programa de servidor pode ser chamado na Internet, em uma intranet, em uma rede local ou pode ser uma biblioteca de vínculo dinâmico local.</span><span class="sxs-lookup"><span data-stu-id="5dd60-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5dd60-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span><span class="sxs-lookup"><span data-stu-id="5dd60-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="5dd60-111">Este objeto representa o programa de servidor padrão.</span><span class="sxs-lookup"><span data-stu-id="5dd60-111">This object represents the default server program.</span></span> <span data-ttu-id="5dd60-112">Ele executa o comportamento padrão de recuperação e atualização de dados RDS.</span><span class="sxs-lookup"><span data-stu-id="5dd60-112">It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5dd60-113"><a href="datacontrol-object-rds.md">RDS. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="5dd60-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="5dd60-114">Este objeto pode chamar automaticamente os objetos <strong>RDS.DataSpace</strong> e <strong>RDSServer.DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="5dd60-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="5dd60-115">Utilize-o para chamar o comportamento padrão de recuperação ou atualização de dados RDS.</span><span class="sxs-lookup"><span data-stu-id="5dd60-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="5dd60-116">Este objeto também permite que controles visuais acessem o objeto <strong>Recordset</strong> retornado.</span><span class="sxs-lookup"><span data-stu-id="5dd60-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

