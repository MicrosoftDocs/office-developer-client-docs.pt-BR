---
title: Propriedade Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 971a528c0efe97626f08ff94490e8aee25230f60
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926532"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="e35af-102">Propriedade Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e35af-102">Name property (ADO MD)</span></span>


<span data-ttu-id="e35af-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="e35af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e35af-104">Indica o nome de um objeto</span><span class="sxs-lookup"><span data-stu-id="e35af-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="e35af-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e35af-105">Return values</span></span>

<span data-ttu-id="e35af-106">Retorna um objeto **String** e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e35af-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e35af-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e35af-107">Remarks</span></span>

<span data-ttu-id="e35af-p101">Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal e, depois, fazer referência ao objeto diretamente pelo nome. Por exemplo, se cdf.CubeDefs(0).Name gerar "Bobs Video Store", você poderá fazer referência a esse [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Bobs Video Store").</span><span class="sxs-lookup"><span data-stu-id="e35af-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

