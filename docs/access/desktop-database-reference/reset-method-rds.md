---
title: Método Reset (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: Reset Method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3932eaab38498b8c82256ceb0de49a9c78030cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463702"
---
# <a name="reset-method-rds"></a><span data-ttu-id="84de4-102">Método Reset (RDS)</span><span class="sxs-lookup"><span data-stu-id="84de4-102">Reset Method (RDS)</span></span>


<span data-ttu-id="84de4-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="84de4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="84de4-104">Executa a classificação ou a filtragem em um **Recordset** de cliente, com base nas propriedades de classificação e filtragem especificadas.</span><span class="sxs-lookup"><span data-stu-id="84de4-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="84de4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84de4-105">Syntax</span></span>

<span data-ttu-id="84de4-106">*DataControl*. Redefinição (*valor*)</span><span class="sxs-lookup"><span data-stu-id="84de4-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="84de4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84de4-107">Parameters</span></span>

  - <span data-ttu-id="84de4-108">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="84de4-108">*DataControl*</span></span>

  - <span data-ttu-id="84de4-109">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="84de4-109">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="84de4-110">*value*</span><span class="sxs-lookup"><span data-stu-id="84de4-110">*value*</span></span>

  - <span data-ttu-id="84de4-p101">Opcional. Um valor **Boolean** que é **True** (padrão) se você deseja filtrar pelo conjunto de linhas "filtrado" atual. **False** indica que você filtra pelo conjunto de linhas original, removendo quaisquer opções de filtro anteriores.</span><span class="sxs-lookup"><span data-stu-id="84de4-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>

## <a name="remarks"></a><span data-ttu-id="84de4-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="84de4-114">Remarks</span></span>

<span data-ttu-id="84de4-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e de filtro no cache do cliente. A funcionalidade de classificação ordena os registros pelos valores de uma coluna. A funcionalidade de filtro exibe um subconjunto de registros com base em critérios de localização, enquanto o [Recordset](recordset-object-ado.md) completo é mantido no cache. O método **Reset** irá executar os critérios e substituir o **Recordset** atual por um **Recordset** atualizável.</span><span class="sxs-lookup"><span data-stu-id="84de4-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="84de4-p103">Se houver alterações nos dados originais que ainda não foram submetidas, o método **Reset** falhará. Primeiro, utilize o método [SubmitChanges](submitchanges-method-rds.md) para salvar quaisquer alterações em um **Recordset** de leitura/gravação e, em seguida, utilize o método **Reset** para classificar ou filtrar os registros.</span><span class="sxs-lookup"><span data-stu-id="84de4-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="84de4-121">Se você quiser executar mais de um filtro no seu conjunto de linhas, você pode usar o opcional argumento *booleano* com o método **Reset** .</span><span class="sxs-lookup"><span data-stu-id="84de4-121">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method.</span></span> <span data-ttu-id="84de4-122">O exemplo a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="84de4-122">The following example shows how to do this:</span></span>

