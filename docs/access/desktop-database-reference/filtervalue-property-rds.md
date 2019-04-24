---
title: Propriedade FilterValue (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292402"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="707cb-102">Propriedade FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="707cb-102">FilterValue property (RDS)</span></span>

<span data-ttu-id="707cb-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="707cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="707cb-104">Indica o valor com o qual os registros são filtrados.</span><span class="sxs-lookup"><span data-stu-id="707cb-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="707cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="707cb-105">Syntax</span></span>

<span data-ttu-id="707cb-106">*DataControl*. FilterValue = *cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="707cb-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="707cb-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="707cb-107">Parameters</span></span>

|<span data-ttu-id="707cb-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="707cb-108">Parameter</span></span>|<span data-ttu-id="707cb-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="707cb-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="707cb-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="707cb-110">*DataControl*</span></span> |<span data-ttu-id="707cb-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="707cb-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="707cb-112">*String*</span><span class="sxs-lookup"><span data-stu-id="707cb-112">*String*</span></span> |<span data-ttu-id="707cb-113">Um valor **String** que representa um valor de dados com o qual os registros são filtrados (por exemplo, ' Programmer ' ou 125).</span><span class="sxs-lookup"><span data-stu-id="707cb-113">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="707cb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="707cb-114">Remarks</span></span>

<span data-ttu-id="707cb-115">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="707cb-115">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache.</span></span> 

<span data-ttu-id="707cb-116">A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna.</span><span class="sxs-lookup"><span data-stu-id="707cb-116">The sorting functionality orders records by values from one column.</span></span> <span data-ttu-id="707cb-117">A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache.</span><span class="sxs-lookup"><span data-stu-id="707cb-117">The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache.</span></span> <span data-ttu-id="707cb-118">O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="707cb-118">The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="707cb-119">Valores nulos resultam em um erro de tipos incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="707cb-119">Null values result in a type mismatch error.</span></span>

