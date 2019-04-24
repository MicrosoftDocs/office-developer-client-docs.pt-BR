---
title: Método Delete (coleção paraMeters do ADO)
TOCTitle: Delete method (ADO Parameters Collection)
ms:assetid: 03ffc24d-fea2-30fa-c8e9-43eb524fd51f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248804(v=office.15)
ms:contentKeyID: 48542998
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e075e176f1c007a258f6277147442223ae108b47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294089"
---
# <a name="delete-method-ado-parameters-collection"></a><span data-ttu-id="9af78-102">Método Delete (coleção paraMeters do ADO)</span><span class="sxs-lookup"><span data-stu-id="9af78-102">Delete method (ADO Parameters Collection)</span></span>

<span data-ttu-id="9af78-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9af78-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9af78-104">Exclui um objeto da coleção [Parameters](parameters-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9af78-104">Deletes an object from the [Parameters](parameters-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af78-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9af78-105">Syntax</span></span>

<span data-ttu-id="9af78-106">*Parâmetros*. Excluir *índice*</span><span class="sxs-lookup"><span data-stu-id="9af78-106">*Parameters*.Delete *Index*</span></span>

## <a name="parameters"></a><span data-ttu-id="9af78-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9af78-107">Parameters</span></span>

|<span data-ttu-id="9af78-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="9af78-108">Parameter</span></span>|<span data-ttu-id="9af78-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="9af78-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9af78-110">*Índice*</span><span class="sxs-lookup"><span data-stu-id="9af78-110">*Index*</span></span> |<span data-ttu-id="9af78-111">Um valor **String** que contém o nome do objeto que você deseja excluir ou a posição ordinal do objeto (índice) na coleção.</span><span class="sxs-lookup"><span data-stu-id="9af78-111">A **String** value that contains the name of the object you want to delete, or the objects ordinal position (index) in the collection.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9af78-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9af78-112">Remarks</span></span>

<span data-ttu-id="9af78-p101">A utilização do método **Delete** em uma coleção permite remover um dos objetos da coleção. Esse método está disponível apenas na coleção **Parameters** de um objeto [Command](command-object-ado.md). Você deve utilizar a propriedade [Name](name-property-ado.md) do objeto [Parameter](parameter-object-ado.md) ou seu índice de coleção ao chamar o método **Delete** — uma variável de objeto não é um argumento válido.</span><span class="sxs-lookup"><span data-stu-id="9af78-p101">Using the **Delete** method on a collection lets you remove one of the objects in the collection. This method is available only on the **Parameters** collection of a [Command](command-object-ado.md) object. You must use the [Parameter](parameter-object-ado.md) object's [Name](name-property-ado.md) property or its collection index when calling the **Delete** method — an object variable is not a valid argument.</span></span>

