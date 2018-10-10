---
title: Propriedade Children (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462540"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="5f172-102">Propriedade Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5f172-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="5f172-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f172-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5f172-104">Retorna uma coleção de [Members](members-collection-ado-md.md) dos quais o [Member](member-object-ado-md.md) atual é o pai na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="5f172-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="5f172-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="5f172-105">Return Values</span></span>

<span data-ttu-id="5f172-106">Retorna uma coleção **Members** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5f172-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f172-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f172-107">Remarks</span></span>

<span data-ttu-id="5f172-p101">A propriedade **Children** contém uma coleção **Members** da qual o **Member** atual é o pai hierárquico. Os objetos **Member** no nível de folha não têm membros filho na coleção **Members**. Essa propriedade só é suportada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md). Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="5f172-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

