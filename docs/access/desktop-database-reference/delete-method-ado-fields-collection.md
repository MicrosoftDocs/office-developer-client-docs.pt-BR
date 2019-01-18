---
title: Excluir método (coleção Fields do ADO)
TOCTitle: Delete method (ADO Fields Collection)
ms:assetid: adc66365-703f-4491-fc5b-dbc9bca2ac53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249817(v=office.15)
ms:contentKeyID: 48547047
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e5d97cec041d69ddbbfe61600ca6b03cb09bc466
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718256"
---
# <a name="delete-method-ado-fields-collection"></a><span data-ttu-id="0ea16-102">Excluir método (coleção Fields do ADO)</span><span class="sxs-lookup"><span data-stu-id="0ea16-102">Delete method (ADO Fields Collection)</span></span>

<span data-ttu-id="0ea16-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ea16-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0ea16-104">Exclui um objeto da coleção [Fields](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0ea16-104">Deletes an object from the [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ea16-105">Syntax</span></span>

<span data-ttu-id="0ea16-106">*Campos*. Excluir um*campo*</span><span class="sxs-lookup"><span data-stu-id="0ea16-106">*Fields*.Delete*Field*</span></span>

## <a name="parameters"></a><span data-ttu-id="0ea16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ea16-107">Parameters</span></span>

|<span data-ttu-id="0ea16-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ea16-108">Parameter</span></span>|<span data-ttu-id="0ea16-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ea16-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0ea16-110">*Field*</span><span class="sxs-lookup"><span data-stu-id="0ea16-110">*Field*</span></span> |<span data-ttu-id="0ea16-p101">Um **Variant** que designa o objeto [Field](field-object-ado.md) a ser excluído. Este parâmetro pode ser o nome do objeto **Field** ou a posição ordinal do próprio objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="0ea16-p101">A **Variant** that designates the [Field](field-object-ado.md) object to delete. This parameter can be the name of the **Field** object or the ordinal position of the **Field** object itself.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0ea16-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea16-113">Remarks</span></span>

<span data-ttu-id="0ea16-114">Chamar o método **Fields.Delete** em um [Recordset](recordset-object-ado.md) aberto causa um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0ea16-114">Calling the **Fields.Delete** method on an open [Recordset](recordset-object-ado.md) causes a run-time error.</span></span>

