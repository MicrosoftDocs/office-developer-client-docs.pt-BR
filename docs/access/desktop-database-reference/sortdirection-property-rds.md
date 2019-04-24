---
title: Propriedade SortDirection (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd09eb22d9f751ab1140db948356d2b168b30afb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308614"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="d89c7-102">Propriedade SortDirection (RDS)</span><span class="sxs-lookup"><span data-stu-id="d89c7-102">SortDirection property (RDS)</span></span>

<span data-ttu-id="d89c7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d89c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d89c7-104">Indica se uma ordem de classificação é crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="d89c7-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89c7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d89c7-105">Syntax</span></span>

<span data-ttu-id="d89c7-106">*DataControl*. SortDirection = *valor*</span><span class="sxs-lookup"><span data-stu-id="d89c7-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="d89c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d89c7-107">Parameters</span></span>

|<span data-ttu-id="d89c7-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="d89c7-108">Parameter</span></span>|<span data-ttu-id="d89c7-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d89c7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d89c7-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d89c7-110">*DataControl*</span></span> |<span data-ttu-id="d89c7-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="d89c7-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="d89c7-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="d89c7-112">*Value*</span></span> |<span data-ttu-id="d89c7-p101">Um valor **Boolean** que, quando definido como **True**, indica a direção da classificação como crescente. **False** indica a ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="d89c7-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d89c7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d89c7-115">Remarks</span></span>

<span data-ttu-id="d89c7-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método **Reset** executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="d89c7-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

