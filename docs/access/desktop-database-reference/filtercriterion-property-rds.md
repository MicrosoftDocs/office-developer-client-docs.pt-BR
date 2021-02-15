---
title: Propriedade FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292423"
---
# <a name="filtercriterion-property-rds"></a><span data-ttu-id="c476d-102">Propriedade FilterCriterion (RDS)</span><span class="sxs-lookup"><span data-stu-id="c476d-102">FilterCriterion property (RDS)</span></span>

<span data-ttu-id="c476d-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c476d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c476d-104">Indica o operador de avaliação a ser usado no valor do filtro.</span><span class="sxs-lookup"><span data-stu-id="c476d-104">Indicates the evaluation operator to use in the filter value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c476d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c476d-105">Syntax</span></span>

<span data-ttu-id="c476d-106">*DataControl*. FilterCriterion = *String*</span><span class="sxs-lookup"><span data-stu-id="c476d-106">*DataControl*.FilterCriterion = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="c476d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c476d-107">Parameters</span></span>

|<span data-ttu-id="c476d-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="c476d-108">Parameter</span></span>|<span data-ttu-id="c476d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c476d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="c476d-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="c476d-110">*DataControl*</span></span> |<span data-ttu-id="c476d-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="c476d-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="c476d-112">*String*</span><span class="sxs-lookup"><span data-stu-id="c476d-112">*String*</span></span> |<span data-ttu-id="c476d-113">Um valor **String** que especifica o operador de avaliação do [FilterValue](filtervalue-property-rds.md) para os registros.</span><span class="sxs-lookup"><span data-stu-id="c476d-113">A **String** value that specifies the evaluation operator of the [FilterValue](filtervalue-property-rds.md) to the records.</span></span> <span data-ttu-id="c476d-114">Pode ser qualquer um dos seguintes: \< , = , = , \< \> \> =, =, ou \< \> .</span><span class="sxs-lookup"><span data-stu-id="c476d-114">Can be any one of the following: \<, \<=, \>, \>=, =, or \<\>.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c476d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c476d-115">Remarks</span></span>

<span data-ttu-id="c476d-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c476d-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**, and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="c476d-120">O operador " \! =" não é válido para **FilterCriterion**; em vez disso, use " \< \> ".</span><span class="sxs-lookup"><span data-stu-id="c476d-120">The "\!=" operator is not valid for **FilterCriterion**; instead, use "\<\>".</span></span>

<span data-ttu-id="c476d-p103">Se tanto as propriedades de filtro como as de classificação estiverem definidas, e o método **Reset** for chamado, o conjunto de linhas será filtrado primeiro e depois classificado. Nas classificações em ordem crescente, os valores nulos ficam na parte superior; nas classificações em ordem decrescente, os valores nulos ficam na parte inferior (a ordem crescente é o comportamento padrão).</span><span class="sxs-lookup"><span data-stu-id="c476d-p103">If both the filter and sort properties are set and you call the **Reset** method, the rowset is first filtered and then it is sorted. For ascending sorts, the null values are at the top; for descending sorts, null values are at the bottom (ascending is default behavior).</span></span>

