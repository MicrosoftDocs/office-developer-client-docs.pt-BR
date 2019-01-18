---
title: Propriedade Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713531"
---
# <a name="count-property-ado"></a><span data-ttu-id="cc8a1-102">Propriedade Count (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc8a1-102">Count property (ADO)</span></span>


<span data-ttu-id="cc8a1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc8a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc8a1-104">Indica a quantidade de objetos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="cc8a1-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc8a1-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="cc8a1-105">Return value</span></span>

<span data-ttu-id="cc8a1-106">Retorna um valor **Long**.</span><span class="sxs-lookup"><span data-stu-id="cc8a1-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc8a1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc8a1-107">Remarks</span></span>

<span data-ttu-id="cc8a1-108">Use a propriedade **Count** para determinar quantos objetos existem em uma determinada coleção.</span><span class="sxs-lookup"><span data-stu-id="cc8a1-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="cc8a1-p101">Como a numeração dos membros de uma coleção começa com zero, você deve sempre codificar loops que comecem no membro zero e terminem com o valor da propriedade **Count** menos 1. Se estiver usando o Microsoft Visual Basic e quiser executar um loop utilizando os membros da coleção sem verificar a propriedade **Count**, use o comando **For** **Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="cc8a1-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="cc8a1-111">Se a propriedade **Count** for zero, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="cc8a1-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

