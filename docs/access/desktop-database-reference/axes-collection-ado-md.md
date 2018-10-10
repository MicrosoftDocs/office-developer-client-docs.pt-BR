---
title: Coleção Axes (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2b078f2d8f1ea6562d6f82f90943923c7d92a07
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464498"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="0a6c5-102">Coleção Axes (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0a6c5-102">Axes Collection (ADO MD)</span></span>


<span data-ttu-id="0a6c5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a6c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a6c5-104">Contém os objetos [Axis](axis-object-ado-md.md) que definem um conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6c5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a6c5-105">Remarks</span></span>

<span data-ttu-id="0a6c5-p101">Um objeto [Cellset](cellset-object-ado-md.md) contém uma coleção **Axes**. Quando um **Cellset** está aberto, essa coleção conterá pelo menos um **Axis**. Consulte o objeto [Axis](axis-object-ado-md.md) para obter uma explicação mais detalhada sobre como usar os objetos **Axis**.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-p101">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection. Once the **Cellset** is opened, this collection will contain at least one **Axis**. See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0a6c5-p102">[!OBSERVAçãO] O eixo de filtro de um <STRONG>Cellset</STRONG> não está contido na coleção <STRONG>Axes</STRONG>. Consulte a propriedade <A href="filteraxis-property-ado-md.md">FilterAxis</A> para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="0a6c5-p102">The filter axis of a <STRONG>Cellset</STRONG> is not contained in the <STRONG>Axes</STRONG> collection. See the <A href="filteraxis-property-ado-md.md">FilterAxis</A> property for more information.</span></span></P>



<span data-ttu-id="0a6c5-p103">**Axes** é uma coleção padrão do ADO. Com as propriedades e os métodos de uma coleção, você pode executar os seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="0a6c5-p103">**Axes** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="0a6c5-113">Obter o número de objetos na coleção com a propriedade [Count](count-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0a6c5-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="0a6c5-114">Retornar um objeto da coleção com a propriedade padrão [Item](item-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0a6c5-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="0a6c5-115">Atualizar os objetos na coleção do provedor com o método [Refresh](refresh-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0a6c5-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

