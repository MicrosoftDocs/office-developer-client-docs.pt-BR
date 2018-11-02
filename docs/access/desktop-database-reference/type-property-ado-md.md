---
title: Propriedade Type (ADO MD)
TOCTitle: Type property (ADO MD)
ms:assetid: 4aaa151e-1f02-aa7d-a9e5-e7019b200924
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249230(v=office.15)
ms:contentKeyID: 48544671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f5cffb5fb888298b23dad02d9593978e581aa6c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928744"
---
# <a name="type-property-ado-md"></a><span data-ttu-id="a83fc-102">Propriedade Type (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a83fc-102">Type property (ADO MD)</span></span>


<span data-ttu-id="a83fc-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a83fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a83fc-104">Indica o tipo do membro atual.</span><span class="sxs-lookup"><span data-stu-id="a83fc-104">Indicates the type of the current member.</span></span>

## <a name="return-values"></a><span data-ttu-id="a83fc-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a83fc-105">Return values</span></span>

<span data-ttu-id="a83fc-106">Retorna um valor [MemberTypeEnum](membertypeenum.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a83fc-106">Returns a [MemberTypeEnum](membertypeenum.md) value and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a83fc-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="a83fc-107">Remarks</span></span>

<span data-ttu-id="a83fc-p101">Somente os objetos [Member](member-object-ado-md.md) pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="a83fc-p101">This property is supported only on [Member](member-object-ado-md.md) objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

