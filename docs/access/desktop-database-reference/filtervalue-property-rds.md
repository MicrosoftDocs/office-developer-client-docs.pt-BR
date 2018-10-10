---
title: Propriedade FilterValue (RDS)
TOCTitle: FilterValue Property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39152be2c53dc0de9bc1bcb21fee505fcb9106dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463137"
---
# <a name="filtervalue-property-rds"></a><span data-ttu-id="f4b6b-102">Propriedade FilterValue (RDS)</span><span class="sxs-lookup"><span data-stu-id="f4b6b-102">FilterValue Property (RDS)</span></span>


<span data-ttu-id="f4b6b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4b6b-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="f4b6b-104">Indica o valor com o qual os registros são filtrados.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-104">Indicates the value with which to filter records.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4b6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4b6b-105">Syntax</span></span>

<span data-ttu-id="f4b6b-106">*DataControl*. FilterValue = *String*</span><span class="sxs-lookup"><span data-stu-id="f4b6b-106">*DataControl*.FilterValue = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="f4b6b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4b6b-107">Parameters</span></span>

  - <span data-ttu-id="f4b6b-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f4b6b-108">*DataControl*</span></span>

  - <span data-ttu-id="f4b6b-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f4b6b-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="f4b6b-110">*String*</span><span class="sxs-lookup"><span data-stu-id="f4b6b-110">*String*</span></span>

  - <span data-ttu-id="f4b6b-111">Um valor **String** que representa um valor de dados com o qual deseja filtrar registros (por exemplo, 'Programmer' ou 125).</span><span class="sxs-lookup"><span data-stu-id="f4b6b-111">A **String** value that represents a data value with which to filter records (for example, 'Programmer' or 125 ).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4b6b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4b6b-112">Remarks</span></span>

<span data-ttu-id="f4b6b-p101">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-p101">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The [Reset](reset-method-rds.md) method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="f4b6b-117">Valores nulos resultam em um erro de tipos incompatíveis.</span><span class="sxs-lookup"><span data-stu-id="f4b6b-117">Null values result in a type mismatch error.</span></span>

