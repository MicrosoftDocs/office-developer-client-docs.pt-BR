---
title: Propriedade FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711781"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="8e2d4-102">Propriedade FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="8e2d4-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="8e2d4-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8e2d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e2d4-104">Indica a coluna em que os critérios de filtro serão avaliados.</span><span class="sxs-lookup"><span data-stu-id="8e2d4-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2d4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e2d4-105">Syntax</span></span>

<span data-ttu-id="8e2d4-106">*DataControl*. FilterColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="8e2d4-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="8e2d4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e2d4-107">Parameters</span></span>

|<span data-ttu-id="8e2d4-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e2d4-108">Parameter</span></span>|<span data-ttu-id="8e2d4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e2d4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8e2d4-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="8e2d4-110">*DataControl*</span></span> |<span data-ttu-id="8e2d4-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8e2d4-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="8e2d4-112">*String*</span><span class="sxs-lookup"><span data-stu-id="8e2d4-112">*String*</span></span> |<span data-ttu-id="8e2d4-p101">Um valor **String** que especifica a coluna em que os critérios de filtro serão avaliados. Os critérios de filtro são especificados na propriedade [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="8e2d4-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8e2d4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e2d4-115">Remarks</span></span>

<span data-ttu-id="8e2d4-116">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e **FilterColumn** fornecem funcionalidade de classificação e filtragem no cache do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e2d4-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="8e2d4-117">A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="8e2d4-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="8e2d4-118">A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache.</span><span class="sxs-lookup"><span data-stu-id="8e2d4-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="8e2d4-119">O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="8e2d4-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

