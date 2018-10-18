---
title: Propriedade Parent (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10c183c997a3c0b49c74e08f7ef29fbe8c274516
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603333"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="d05c5-102">Propriedade Parent (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d05c5-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="d05c5-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d05c5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d05c5-104">Indica o membro que é o pai do membro atual em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="d05c5-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

<span data-ttu-id="d05c5-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="d05c5-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="d05c5-106">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="d05c5-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="d05c5-107">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d05c5-107">Return values</span></span>
>>>>>>> <span data-ttu-id="d05c5-108">mestre</span><span class="sxs-lookup"><span data-stu-id="d05c5-108">master</span></span>

<span data-ttu-id="d05c5-109">Retorna um objeto [Member](member-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d05c5-109">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d05c5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d05c5-110">Remarks</span></span>

<span data-ttu-id="d05c5-p101">Um membro que está no nível superior de uma hierarquia (a raiz) não tem pai. Somente objetos **Member** pertencentes a um objeto [Level](level-object-ado-md.md) oferecem suporte a esta propriedade. Ocorre um erro quando essa propriedade é referenciada em objetos **Member** pertencentes a um objeto [Position](position-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="d05c5-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

