---
title: Propriedade Parent (ADO MD)
TOCTitle: Parent property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1da5b763d85fc9975a42e357860d87ce64cf618
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930585"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="ba51b-102">Propriedade Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ba51b-102">Parent property (ADO MD)</span></span>


<span data-ttu-id="ba51b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba51b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba51b-104">Indica o membro que é o pai do membro atual em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="ba51b-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="ba51b-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ba51b-105">Return values</span></span>

<span data-ttu-id="ba51b-106">Retorna um objeto [Member](member-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ba51b-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba51b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba51b-107">Remarks</span></span>

<span data-ttu-id="ba51b-p101">Um membro que está no nível superior de uma hierarquia (a raiz) não tem pai. Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ba51b-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

