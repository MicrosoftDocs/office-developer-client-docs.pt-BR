---
title: InheritTypeEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860564"
---
# <a name="inherittypeenum"></a><span data-ttu-id="5840e-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="5840e-102">InheritTypeEnum</span></span>

<span data-ttu-id="5840e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5840e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5840e-104">Especifica como os objetos herdarão permissões definidas com [SetPermissions](setpermissions-method-adox.md).</span><span class="sxs-lookup"><span data-stu-id="5840e-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5840e-105">Constant</span><span class="sxs-lookup"><span data-stu-id="5840e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5840e-106">Valor</span><span class="sxs-lookup"><span data-stu-id="5840e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5840e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5840e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5840e-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="5840e-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="5840e-109">3</span><span class="sxs-lookup"><span data-stu-id="5840e-109">3</span></span></p></td>
<td><p><span data-ttu-id="5840e-110">Os objetos e os outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="5840e-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5840e-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="5840e-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="5840e-112">2</span><span class="sxs-lookup"><span data-stu-id="5840e-112">2</span></span></p></td>
<td><p><span data-ttu-id="5840e-113">Outros contêineres existentes no objeto principal herdam a entrada.</span><span class="sxs-lookup"><span data-stu-id="5840e-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5840e-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="5840e-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="5840e-115">0</span><span class="sxs-lookup"><span data-stu-id="5840e-115">0</span></span></p></td>
<td><p><span data-ttu-id="5840e-p101">Padrão. Nada é herdado.</span><span class="sxs-lookup"><span data-stu-id="5840e-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5840e-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="5840e-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="5840e-119">4</span><span class="sxs-lookup"><span data-stu-id="5840e-119">4</span></span></p></td>
<td><p><span data-ttu-id="5840e-120">Os sinalizadores <strong>adInheritObjects</strong> e <strong>adInheritContainers</strong> não são propagados para uma entrada herdada.</span><span class="sxs-lookup"><span data-stu-id="5840e-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5840e-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="5840e-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="5840e-122">1</span><span class="sxs-lookup"><span data-stu-id="5840e-122">1</span></span></p></td>
<td><p><span data-ttu-id="5840e-123">Os objetos não contêiner existentes no contêiner herdam as permissões.</span><span class="sxs-lookup"><span data-stu-id="5840e-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

