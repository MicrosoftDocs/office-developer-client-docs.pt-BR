---
title: Propriedade SortDirection (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0db4bd5661bc32cb6f9ce8191dd4ac5bad7eff4c
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950108"
---
# <a name="sortdirection-property-rds"></a><span data-ttu-id="4c1d1-102">Propriedade SortDirection (RDS)</span><span class="sxs-lookup"><span data-stu-id="4c1d1-102">SortDirection property (RDS)</span></span>

<span data-ttu-id="4c1d1-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c1d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4c1d1-104">Indica se uma ordem de classificação é crescente ou decrescente.</span><span class="sxs-lookup"><span data-stu-id="4c1d1-104">Indicates whether a sort order is ascending or descending.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c1d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c1d1-105">Syntax</span></span>

<span data-ttu-id="4c1d1-106">*DataControl*. SortDirection = *value*</span><span class="sxs-lookup"><span data-stu-id="4c1d1-106">*DataControl*.SortDirection = *value*</span></span>

## <a name="parameters"></a><span data-ttu-id="4c1d1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c1d1-107">Parameters</span></span>

|<span data-ttu-id="4c1d1-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c1d1-108">Parameter</span></span>|<span data-ttu-id="4c1d1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c1d1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4c1d1-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="4c1d1-110">*DataControl*</span></span> |<span data-ttu-id="4c1d1-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="4c1d1-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="4c1d1-112">*Valor*</span><span class="sxs-lookup"><span data-stu-id="4c1d1-112">*Value*</span></span> |<span data-ttu-id="4c1d1-p101">Um valor **Boolean** que, quando definido como **True**, indica a direção da classificação como crescente. **False** indica a ordem decrescente.</span><span class="sxs-lookup"><span data-stu-id="4c1d1-p101">A **Boolean** value that, when set to **True**, indicates the sort direction is ascending. **False** indicates descending order.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4c1d1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c1d1-115">Remarks</span></span>

<span data-ttu-id="4c1d1-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método **Reset** executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="4c1d1-p102">The [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

