---
title: Método Delete (Coleção Parameters do ADO)
TOCTitle: Delete Method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 43d193a78be10ec5cedc2fe1a4001e677878dfb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464203"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="cac8a-102">Método Delete (Coleção Parameters do ADO)</span><span class="sxs-lookup"><span data-stu-id="cac8a-102">Delete Method (ADO Parameters Collection)</span></span>


<span data-ttu-id="cac8a-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cac8a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="cac8a-104">Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cac8a-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac8a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cac8a-105">Syntax</span></span>

<span data-ttu-id="cac8a-106">*Parâmetros*. Excluir *índice*</span><span class="sxs-lookup"><span data-stu-id="cac8a-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="cac8a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cac8a-107">Parameters</span></span>

  - <span data-ttu-id="cac8a-108">*Index*</span><span class="sxs-lookup"><span data-stu-id="cac8a-108">*Index*</span></span>

  - <span data-ttu-id="cac8a-109">Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.</span><span class="sxs-lookup"><span data-stu-id="cac8a-109">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="cac8a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cac8a-110">Remarks</span></span>

<span data-ttu-id="cac8a-p101">A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](parameter-object-ado.md) do objeto [Parameter](name-property-ado.md) ou seu índice de coleção ao chamar o método **Delete**  uma variável de objeto não é um argumento válido.</span><span class="sxs-lookup"><span data-stu-id="cac8a-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

