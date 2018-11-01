---
title: Propriedade Children (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875207"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="ffa23-102">Propriedade Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ffa23-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="ffa23-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ffa23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ffa23-104">Retorna uma coleção de [Members](members-collection-ado-md.md) dos quais o [Member](member-object-ado-md.md) atual é o pai na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="ffa23-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="ffa23-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ffa23-105">Return values</span></span>

<span data-ttu-id="ffa23-106">Retorna uma coleção **Members** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ffa23-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa23-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ffa23-107">Remarks</span></span>

<span data-ttu-id="ffa23-p101">A propriedade **Children** contém uma coleção **Members** da qual o **Member** atual é o pai hierárquico. Os objetos **Member** no nível de folha não têm membros filho na coleção **Members**. Essa propriedade só é suportada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md). Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ffa23-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

