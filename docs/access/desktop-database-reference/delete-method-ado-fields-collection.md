---
title: Método Delete (Coleção Fields do ADO)
TOCTitle: Delete Method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fc2e614916026effe6ee0a9766e0b23db200574
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886393"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="6d248-102">Método Delete (Coleção Fields do ADO)</span><span class="sxs-lookup"><span data-stu-id="6d248-102">Delete Method (ADO Fields Collection)</span></span>


<span data-ttu-id="6d248-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d248-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="6d248-104">Exclui um objeto da coleção [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6d248-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d248-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d248-105">Syntax</span></span>

<span data-ttu-id="6d248-106">*Campos*. Excluir um*campo*</span><span class="sxs-lookup"><span data-stu-id="6d248-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="6d248-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d248-107">Parameters</span></span>

  - <span data-ttu-id="6d248-108">*Field*</span><span class="sxs-lookup"><span data-stu-id="6d248-108">*Field*</span></span>

  - <span data-ttu-id="6d248-p101">Um **Variant** que designa o objeto [Field](field-object-ado.md) a ser excluído. Este parâmetro pode ser o nome do objeto **Field** ou a posição ordinal do próprio objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="6d248-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d248-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d248-111">Remarks</span></span>

<span data-ttu-id="6d248-112">Chamar o método **Fields.Delete** em um [Recordset](recordset-object-ado.md) aberto causa um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="6d248-112">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

