---
title: Propriedade Children (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbbae74ce8ce22255e97403fc3906dd50f36b38b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605048"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="952f0-102">Propriedade Children (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="952f0-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="952f0-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="952f0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="952f0-104">Retorna uma coleção de [Members](members-collection-ado-md.md) dos quais o [Member](member-object-ado-md.md) atual é o pai na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="952f0-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

<span data-ttu-id="952f0-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="952f0-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="952f0-106">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="952f0-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="952f0-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="952f0-107">Return values</span></span>
>>>>>>> <span data-ttu-id="952f0-108">mestre</span><span class="sxs-lookup"><span data-stu-id="952f0-108">master</span></span>

<span data-ttu-id="952f0-109">Retorna uma coleção **Members** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="952f0-109">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="952f0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="952f0-110">Remarks</span></span>

<span data-ttu-id="952f0-p101">A propriedade **Children** contém uma coleção **Members** da qual o **Member** atual é o pai hierárquico. Os objetos **Member** no nível de folha não têm membros filho na coleção **Members**. Essa propriedade só é suportada em objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md). Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="952f0-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

