---
title: InheritTypeEnum (referência do banco de dados de área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291411"
---
# <a name="inherittypeenum"></a><span data-ttu-id="aadf3-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="aadf3-102">InheritTypeEnum</span></span>

<span data-ttu-id="aadf3-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aadf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aadf3-104">Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="aadf3-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aadf3-105">Constant</span><span class="sxs-lookup"><span data-stu-id="aadf3-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aadf3-106">Valor</span><span class="sxs-lookup"><span data-stu-id="aadf3-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aadf3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="aadf3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aadf3-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="aadf3-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="aadf3-109">3D</span><span class="sxs-lookup"><span data-stu-id="aadf3-109">3</span></span></p></td>
<td><p><span data-ttu-id="aadf3-110">Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="aadf3-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aadf3-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="aadf3-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="aadf3-112">duas</span><span class="sxs-lookup"><span data-stu-id="aadf3-112">2</span></span></p></td>
<td><p><span data-ttu-id="aadf3-113">Outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="aadf3-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aadf3-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="aadf3-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="aadf3-115">,0</span><span class="sxs-lookup"><span data-stu-id="aadf3-115">0</span></span></p></td>
<td><p><span data-ttu-id="aadf3-p101">Padrão. Nada é herdado.</span><span class="sxs-lookup"><span data-stu-id="aadf3-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aadf3-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="aadf3-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="aadf3-119">quatro</span><span class="sxs-lookup"><span data-stu-id="aadf3-119">4</span></span></p></td>
<td><p><span data-ttu-id="aadf3-120">Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</span><span class="sxs-lookup"><span data-stu-id="aadf3-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aadf3-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="aadf3-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="aadf3-122">1</span><span class="sxs-lookup"><span data-stu-id="aadf3-122">1</span></span></p></td>
<td><p><span data-ttu-id="aadf3-123">Os objetos não contêiner existentes no contêiner herdam as permissões.</span><span class="sxs-lookup"><span data-stu-id="aadf3-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

