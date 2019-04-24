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
# <a name="filtercolumn-property-rds"></a>Propriedade FilterColumn (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Indica a coluna em que os critérios de filtro serão avaliados.

## <a name="syntax"></a>Sintaxe

*DataControl*. FilterColumn = *cadeia de caracteres*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Um valor **String** que especifica a coluna em que os critérios de filtro serão avaliados. Os critérios de filtro são especificados na propriedade [FilterCriterion](filtercriterion-property-rds.md).|

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e **FilterColumn** fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. 

A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. 

O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

