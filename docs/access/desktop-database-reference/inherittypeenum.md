---
title: InheritTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462483"
---
# <a name="inherittypeenum"></a><span data-ttu-id="6841b-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="6841b-102">InheritTypeEnum</span></span>


<span data-ttu-id="6841b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6841b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6841b-104">Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6841b-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6841b-105">Constant</span><span class="sxs-lookup"><span data-stu-id="6841b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6841b-106">Valor</span><span class="sxs-lookup"><span data-stu-id="6841b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6841b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="6841b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6841b-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="6841b-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="6841b-109">3</span><span class="sxs-lookup"><span data-stu-id="6841b-109">3</span></span></p></td>
<td><p><span data-ttu-id="6841b-110">Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="6841b-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6841b-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="6841b-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="6841b-112">2</span><span class="sxs-lookup"><span data-stu-id="6841b-112">2</span></span></p></td>
<td><p><span data-ttu-id="6841b-113">Outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="6841b-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6841b-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="6841b-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6841b-115">0</span><span class="sxs-lookup"><span data-stu-id="6841b-115">0</span></span></p></td>
<td><p><span data-ttu-id="6841b-p101">Padrão. Nada é herdado.</span><span class="sxs-lookup"><span data-stu-id="6841b-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6841b-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="6841b-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="6841b-119">4</span><span class="sxs-lookup"><span data-stu-id="6841b-119">4</span></span></p></td>
<td><p><span data-ttu-id="6841b-120">Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</span><span class="sxs-lookup"><span data-stu-id="6841b-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6841b-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="6841b-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="6841b-122">1</span><span class="sxs-lookup"><span data-stu-id="6841b-122">1</span></span></p></td>
<td><p><span data-ttu-id="6841b-123">Os objetos não contêiner existentes no contêiner herdam as permissões.</span><span class="sxs-lookup"><span data-stu-id="6841b-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

