---
title: InheritTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706804"
---
# <a name="inherittypeenum"></a><span data-ttu-id="18d49-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="18d49-102">InheritTypeEnum</span></span>

<span data-ttu-id="18d49-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="18d49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18d49-104">Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="18d49-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18d49-105">Constant</span><span class="sxs-lookup"><span data-stu-id="18d49-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="18d49-106">Valor</span><span class="sxs-lookup"><span data-stu-id="18d49-106">Value</span></span></p></th>
<th><p><span data-ttu-id="18d49-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="18d49-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18d49-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="18d49-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="18d49-109">3</span><span class="sxs-lookup"><span data-stu-id="18d49-109">3</span></span></p></td>
<td><p><span data-ttu-id="18d49-110">Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="18d49-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d49-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="18d49-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="18d49-112">2</span><span class="sxs-lookup"><span data-stu-id="18d49-112">2</span></span></p></td>
<td><p><span data-ttu-id="18d49-113">Outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="18d49-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d49-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="18d49-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="18d49-115">0</span><span class="sxs-lookup"><span data-stu-id="18d49-115">0</span></span></p></td>
<td><p><span data-ttu-id="18d49-p101">Padrão. Nada é herdado.</span><span class="sxs-lookup"><span data-stu-id="18d49-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d49-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="18d49-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="18d49-119">4</span><span class="sxs-lookup"><span data-stu-id="18d49-119">4</span></span></p></td>
<td><p><span data-ttu-id="18d49-120">Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</span><span class="sxs-lookup"><span data-stu-id="18d49-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d49-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="18d49-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="18d49-122">1</span><span class="sxs-lookup"><span data-stu-id="18d49-122">1</span></span></p></td>
<td><p><span data-ttu-id="18d49-123">Os objetos não contêiner existentes no contêiner herdam as permissões.</span><span class="sxs-lookup"><span data-stu-id="18d49-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

