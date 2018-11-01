---
title: Método Delete (Coleção Parameters do ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e519d40a081b132cd09030e9ba97de9e8987af99
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881955"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="ab372-102">Método Delete (Coleção Parameters do ADO)</span><span class="sxs-lookup"><span data-stu-id="ab372-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="ab372-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab372-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ab372-104">Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ab372-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab372-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab372-105">Syntax</span></span>

<span data-ttu-id="ab372-106">*Parâmetros*. Excluir *índice*</span><span class="sxs-lookup"><span data-stu-id="ab372-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="ab372-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab372-107">Parameters</span></span>

  - <span data-ttu-id="ab372-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="ab372-108">*Index*</span></span>

  - <span data-ttu-id="ab372-109">Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.</span><span class="sxs-lookup"><span data-stu-id="ab372-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab372-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab372-110">Remarks</span></span>

<span data-ttu-id="ab372-p101">A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](parameter-object-ado.md) do objeto [Parameter](name-property-ado.md) ou seu índice de coleção ao chamar o método **Delete**  uma variável de objeto não é um argumento válido.</span><span class="sxs-lookup"><span data-stu-id="ab372-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

