---
title: Método Delete (Coleção Fields do ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294103"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="eab0d-102">Método Delete (Coleção Fields do ADO)</span><span class="sxs-lookup"><span data-stu-id="eab0d-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="eab0d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eab0d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="eab0d-104">Exclui um objeto da coleção [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="eab0d-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab0d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eab0d-105">Syntax</span></span>

<span data-ttu-id="eab0d-106">*Campos*. Excluir *Campo*</span><span class="sxs-lookup"><span data-stu-id="eab0d-106">*Fields*.Delete *Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="eab0d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eab0d-107">Parameters</span></span>

|<span data-ttu-id="eab0d-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="eab0d-108">Parameter</span></span>|<span data-ttu-id="eab0d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="eab0d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="eab0d-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="eab0d-110">*Field*</span></span> |<span data-ttu-id="eab0d-p101">Um **Variant** que designa o objeto [Field](field-object-ado.md) a ser excluído. Este parâmetro pode ser o nome do objeto **Field** ou a posição ordinal do próprio objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="eab0d-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="eab0d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="eab0d-113">Remarks</span></span>

<span data-ttu-id="eab0d-114">Chamar o método **Fields.Delete** em um [Recordset](recordset-object-ado.md) aberto causa um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="eab0d-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

