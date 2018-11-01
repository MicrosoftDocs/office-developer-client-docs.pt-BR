---
title: Mantendo recordsets hierárquicos e filtrados
TOCTitle: Persisting Filtered and Hierarchical Recordsets
ms:assetid: 3648a997-dac7-d8a3-3cca-a6827f26a4f0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249120(v=office.15)
ms:contentKeyID: 48544162
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 931345aff0cd3d8c9b10c53073e640b3cfdd5de5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889711"
---
# <a name="persisting-filtered-and-hierarchical-recordsets"></a><span data-ttu-id="e1116-102">Mantendo recordsets hierárquicos e filtrados</span><span class="sxs-lookup"><span data-stu-id="e1116-102">Persisting Filtered and Hierarchical Recordsets</span></span>


<span data-ttu-id="e1116-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1116-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1116-p101">Se a propriedade [Filter](filter-property-ado.md) estiver em vigor para o **Recordset**, somente as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e todos seus filhos serão salvos, mas o pai não será. Para obter mais informações sobre **Recordsets** hierárquicos, consulte o [Capítulo 9: Data Shaping](chapter-9-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="e1116-p101">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not. For more information about hierarchical **Recordsets**, see [Chapter 9: Data Shaping](chapter-9-data-shaping.md).</span></span>


> [!NOTE]
> <P><span data-ttu-id="e1116-p102">[!OBSERVAçãO] Algumas limitações se aplicam ao salvar <STRONG>Recordsets</STRONG> hierárquicos (formas de dados) em formato XML. Para obter mais informações, consulte <A href="hierarchical-recordsets-in-xml.md">Recordsets hierárquicos em XML</A>.</span><span class="sxs-lookup"><span data-stu-id="e1116-p102">Some limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. For more information, see <A href="hierarchical-recordsets-in-xml.md">Hierarchical Recordsets in XML</A>.</span></span></P>


