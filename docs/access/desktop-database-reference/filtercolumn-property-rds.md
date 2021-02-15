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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292437"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="3aecf-102">Propriedade FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="3aecf-102">FilterColumn property (RDS)</span></span>

<span data-ttu-id="3aecf-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3aecf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3aecf-104">Indica a coluna em que os critérios de filtro serão avaliados.</span><span class="sxs-lookup"><span data-stu-id="3aecf-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aecf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aecf-105">Syntax</span></span>

<span data-ttu-id="3aecf-106">*DataControl*. FilterColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="3aecf-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="3aecf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aecf-107">Parameters</span></span>

|<span data-ttu-id="3aecf-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aecf-108">Parameter</span></span>|<span data-ttu-id="3aecf-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aecf-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3aecf-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="3aecf-110">*DataControl*</span></span> |<span data-ttu-id="3aecf-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3aecf-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="3aecf-112">*String*</span><span class="sxs-lookup"><span data-stu-id="3aecf-112">*String*</span></span> |<span data-ttu-id="3aecf-p101">Um valor **String** que especifica a coluna em que os critérios de filtro serão avaliados. Os critérios de filtro são especificados na propriedade [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="3aecf-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3aecf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aecf-115">Remarks</span></span>

<span data-ttu-id="3aecf-116">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e **FilterColumn** fornecem funcionalidade de classificação e filtragem no cache do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="3aecf-116">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="3aecf-117">A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="3aecf-117">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="3aecf-118">A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache.</span><span class="sxs-lookup"><span data-stu-id="3aecf-118">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> 

<span data-ttu-id="3aecf-119">O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="3aecf-119">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

