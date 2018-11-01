---
title: InheritTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: df631319abc1eba06d7ac804b6d8dbdaf5fc9b18
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888045"
---
# <a name="inherittypeenum"></a><span data-ttu-id="12ad5-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="12ad5-102">InheritTypeEnum</span></span>

<span data-ttu-id="12ad5-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="12ad5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12ad5-104">Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="12ad5-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="12ad5-105">Constant</span><span class="sxs-lookup"><span data-stu-id="12ad5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="12ad5-106">Valor</span><span class="sxs-lookup"><span data-stu-id="12ad5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="12ad5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="12ad5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="12ad5-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="12ad5-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="12ad5-109">3</span><span class="sxs-lookup"><span data-stu-id="12ad5-109">3</span></span></p></td>
<td><p><span data-ttu-id="12ad5-110">Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="12ad5-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12ad5-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="12ad5-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="12ad5-112">2</span><span class="sxs-lookup"><span data-stu-id="12ad5-112">2</span></span></p></td>
<td><p><span data-ttu-id="12ad5-113">Outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="12ad5-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12ad5-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="12ad5-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="12ad5-115">0</span><span class="sxs-lookup"><span data-stu-id="12ad5-115">0</span></span></p></td>
<td><p><span data-ttu-id="12ad5-p101">Padrão. Nada é herdado.</span><span class="sxs-lookup"><span data-stu-id="12ad5-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="12ad5-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="12ad5-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="12ad5-119">4</span><span class="sxs-lookup"><span data-stu-id="12ad5-119">4</span></span></p></td>
<td><p><span data-ttu-id="12ad5-120">Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</span><span class="sxs-lookup"><span data-stu-id="12ad5-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="12ad5-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="12ad5-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="12ad5-122">1</span><span class="sxs-lookup"><span data-stu-id="12ad5-122">1</span></span></p></td>
<td><p><span data-ttu-id="12ad5-123">Os objetos não contêiner existentes no contêiner herdam as permissões.</span><span class="sxs-lookup"><span data-stu-id="12ad5-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

