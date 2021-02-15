---
title: Método Reset (RDS – referência do banco de dados da área de trabalho do Access)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306640"
---
# <a name="reset-method-rds"></a><span data-ttu-id="f8e94-102">Método Reset (RDS)</span><span class="sxs-lookup"><span data-stu-id="f8e94-102">Reset method (RDS)</span></span>

<span data-ttu-id="f8e94-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8e94-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8e94-104">Executa a classificação ou a filtragem em um **Recordset** de cliente, com base nas propriedades de classificação e filtragem especificadas.</span><span class="sxs-lookup"><span data-stu-id="f8e94-104">Executes the sort or filter on a client-side **Recordset** based on the specified sort and filter properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8e94-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8e94-105">Syntax</span></span>

<span data-ttu-id="f8e94-106">*DataControl*. Reset(*value*)</span><span class="sxs-lookup"><span data-stu-id="f8e94-106">*DataControl*.Reset(*value*)</span></span>

## <a name="parameters"></a><span data-ttu-id="f8e94-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8e94-107">Parameters</span></span>

|<span data-ttu-id="f8e94-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8e94-108">Parameter</span></span>|<span data-ttu-id="f8e94-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8e94-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f8e94-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f8e94-110">*DataControl*</span></span> |<span data-ttu-id="f8e94-111">Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="f8e94-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="f8e94-112">*value*</span><span class="sxs-lookup"><span data-stu-id="f8e94-112">*value*</span></span> |<span data-ttu-id="f8e94-p101">Opcional. Um valor **Boolean** que é **True** (padrão) se você deseja filtrar pelo conjunto de linhas "filtrado" atual. **False** indica que você filtra pelo conjunto de linhas original, removendo quaisquer opções de filtro anteriores.</span><span class="sxs-lookup"><span data-stu-id="f8e94-p101">Optional. A **Boolean** value that is **True** (default) if you want to filter on the current "filtered" rowset. **False** indicates that you filter on the original rowset, removing any previous filter options.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f8e94-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8e94-116">Remarks</span></span>

<span data-ttu-id="f8e94-p102">As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e de filtro no cache do cliente. A funcionalidade de classificação ordena os registros pelos valores de uma coluna. A funcionalidade de filtro exibe um subconjunto de registros com base em critérios de localização, enquanto o [Recordset](recordset-object-ado.md) completo é mantido no cache. O método **Reset** irá executar os critérios e substituir o **Recordset** atual por um **Recordset** atualizável.</span><span class="sxs-lookup"><span data-stu-id="f8e94-p102">The [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md), and [FilterColumn](filtercolumn-property-rds.md) properties provide sorting and filtering functionality on the client-side cache. The sorting functionality orders records by values from one column. The filtering functionality displays a subset of records based on a find criteria, while the full [Recordset](recordset-object-ado.md) is maintained in the cache. The **Reset** method will execute the criteria and replace the current **Recordset** with an updatable **Recordset**.</span></span>

<span data-ttu-id="f8e94-p103">Se houver alterações nos dados originais que ainda não foram submetidas, o método **Reset** falhará. Primeiro, utilize o método [SubmitChanges](submitchanges-method-rds.md) para salvar quaisquer alterações em um **Recordset** de leitura/gravação e, em seguida, utilize o método **Reset** para classificar ou filtrar os registros.</span><span class="sxs-lookup"><span data-stu-id="f8e94-p103">If there are changes to the original data that haven't yet been submitted, the **Reset** method will fail. First, use the [SubmitChanges](submitchanges-method-rds.md) method to save any changes in a read/write **Recordset**, and then use the **Reset** method to sort or filter the records.</span></span>

<span data-ttu-id="f8e94-p104">Se você deseja executar mais de um filtro em seu conjunto de linhas, poderá utilizar o argumento opcional *Boolean* com o método **Reset**. O exemplo a seguir mostra como fazer isso:</span><span class="sxs-lookup"><span data-stu-id="f8e94-p104">If you want to perform more than one filter on your rowset, you can use the optional *Boolean* argument with the **Reset** method. The following example shows how to do this:</span></span>

