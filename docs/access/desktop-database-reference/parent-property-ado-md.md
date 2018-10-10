---
title: Propriedade Parent (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb1606a745cb8572f54b253bdbbbbbb461cfc74a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463200"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="d9061-102">Propriedade Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d9061-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="d9061-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9061-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9061-104">Indica o membro que é o pai do membro atual em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d9061-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="d9061-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d9061-105">Return Values</span></span>

<span data-ttu-id="d9061-106">Retorna um objeto [Member](member-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d9061-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9061-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9061-107">Remarks</span></span>

<span data-ttu-id="d9061-p101">Um membro que está no nível superior de uma hierarquia (a raiz) não tem pai. Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d9061-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

