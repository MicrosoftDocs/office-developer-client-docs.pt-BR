---
title: Propriedade ChildCount (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8a55f54bfe796f9dfa0fc3ec157c8f7cfe9fa11
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925216"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="a53c1-102">Propriedade ChildCount (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a53c1-102">ChildCount property (ADO MD)</span></span>


<span data-ttu-id="a53c1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a53c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a53c1-104">Indica o número de membros dos quais o objeto [Member](member-object-ado-md.md) atual é o pai em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="a53c1-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="a53c1-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a53c1-105">Return values</span></span>

<span data-ttu-id="a53c1-106">Retorna um inteiro **Long** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a53c1-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a53c1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a53c1-107">Remarks</span></span>

<span data-ttu-id="a53c1-p101">Use a propriedade **ChildCount** para retornar uma estimativa de quantos filhos pertencem a um **Member**. Os filhos reais de um **Member** podem ser retornados pela propriedade [Children](children-property-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a53c1-p101">Use the **ChildCount** property to return an estimate of how many children a **Member** has. The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="a53c1-p102">No caso de objetos **Member** de um objeto [Position](position-object-ado-md.md), o número máximo retornado é 65536. Se o número real de filhos exceder 65536, o valor retornado ainda será 65536. Portanto, o aplicativo deverá interpretar um **ChildCount** de 65536 como igual ou maior que o número de filhos de 65536.</span><span class="sxs-lookup"><span data-stu-id="a53c1-p102">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536. If the actual number of children exceeds 65536, the value returned will still be 65536. Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="a53c1-p103">No caso de objetos **Member** de um objeto [Level](level-object-ado-md.md), use a propriedade [Count](count-property-ado.md) da coleção ADO na coleção **Children** para determinar o número exato de filhos. A determinação desse número poderá ser lenta se ele for grande na coleção.</span><span class="sxs-lookup"><span data-stu-id="a53c1-p103">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children. Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

