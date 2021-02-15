---
title: Propriedade Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288655"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="1bd8a-102">Propriedade Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1bd8a-102">Name property (ADO MD)</span></span>


<span data-ttu-id="1bd8a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bd8a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bd8a-104">Indica o nome de um objeto</span><span class="sxs-lookup"><span data-stu-id="1bd8a-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="1bd8a-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1bd8a-105">Return values</span></span>

<span data-ttu-id="1bd8a-106">Retorna **String** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd8a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bd8a-107">Remarks</span></span>

<span data-ttu-id="1bd8a-p101">Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").</span><span class="sxs-lookup"><span data-stu-id="1bd8a-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

