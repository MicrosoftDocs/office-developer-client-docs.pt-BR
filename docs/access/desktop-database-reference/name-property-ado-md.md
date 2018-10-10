---
title: Propriedade Name (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462755"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="0de3c-102">Propriedade Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0de3c-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="0de3c-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0de3c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0de3c-104">Indica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0de3c-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="0de3c-105">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0de3c-105">Return Values</span></span>

<span data-ttu-id="0de3c-106">Retorna um objeto **String** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="0de3c-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de3c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0de3c-107">Remarks</span></span>

<span data-ttu-id="0de3c-p101">Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").</span><span class="sxs-lookup"><span data-stu-id="0de3c-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

