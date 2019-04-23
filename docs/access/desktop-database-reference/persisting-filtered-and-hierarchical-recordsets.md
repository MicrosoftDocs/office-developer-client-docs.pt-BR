---
title: Conjuntos de registros persistentes filtrados e hierárquicos
TOCTitle: Persisting filtered and hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1332d4348c993f94d8b2ee61280b8b35c02324c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287584"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="0d4e6-102">Conjuntos de registros persistentes filtrados e hierárquicos</span><span class="sxs-lookup"><span data-stu-id="0d4e6-102">Persisting filtered and hierarchical Recordsets</span></span>


<span data-ttu-id="0d4e6-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d4e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d4e6-p101">Se a propriedade [Filter](filter-property-ado.md) estiver em vigor para o **Recordset**, somente as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e todos seus filhos serão salvos, mas o pai não será. Para obter mais informações sobre **Recordsets** hierárquicos, consulte o [Capítulo 9: Data Shaping](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="0d4e6-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <span data-ttu-id="0d4e6-p102">[!OBSERVAçãO] Algumas limitações se aplicam ao salvar **Recordsets** hierárquicos (formas de dados) em formato XML. Para obter mais informações, consulte [Recordsets hierárquicos em XML](hierarchical-recordsets-in-xml.md).</span><span class="sxs-lookup"><span data-stu-id="0d4e6-p102">Some limitations apply when saving hierarchical **Recordsets** (data shapes) in XML format. For more information, see [Hierarchical Recordsets in XML](hierarchical-recordsets-in-xml.md).</span></span>


