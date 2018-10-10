---
title: Propriedade FilterColumn (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459fc61dbb8c8b1eecffdea3d2c5d2f105b9212a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462814"
---
# <a name="filtercolumn-property-rds"></a><span data-ttu-id="5e1de-102">Propriedade FilterColumn (RDS)</span><span class="sxs-lookup"><span data-stu-id="5e1de-102">FilterColumn Property (RDS)</span></span>


<span data-ttu-id="5e1de-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e1de-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="5e1de-104">Indica a coluna em que os critérios de filtro serão avaliados.</span><span class="sxs-lookup"><span data-stu-id="5e1de-104">Indicates the column on which to evaluate the filter criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e1de-105">Syntax</span></span>

<span data-ttu-id="5e1de-106">*DataControl*. FilterColumn = *String*</span><span class="sxs-lookup"><span data-stu-id="5e1de-106">*DataControl*.FilterColumn = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="5e1de-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e1de-107">Parameters</span></span>

  - <span data-ttu-id="5e1de-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5e1de-108">*DataControl*</span></span>

  - <span data-ttu-id="5e1de-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5e1de-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="5e1de-110">*String*</span><span class="sxs-lookup"><span data-stu-id="5e1de-110">*String*</span></span>

  - <span data-ttu-id="5e1de-p101">Um valor **String** que especifica a coluna em que os critérios de filtro serão avaliados. Os critérios de filtro são especificados na propriedade [FilterCriterion](filtercriterion-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5e1de-p101">A **String** value that specifies the column on which to evaluate the filter criteria. The filter criteria are specified in the [FilterCriterion](filtercriterion-property-rds.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e1de-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e1de-113">Remarks</span></span>

<span data-ttu-id="5e1de-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e **FilterColumn** fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="5e1de-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and **FilterColumn** properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

