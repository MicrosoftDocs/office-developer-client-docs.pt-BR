---
title: Propriedade FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9887551d4d8a141c8390764bcd23c98c59edc26
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950220"
---
# <a name="filtercriterion-property-rds"></a>Propriedade FilterCriterion (RDS)

**Aplica-se a**: Access 2013, o Office 2013

Indica o operador de avaliação a ser usado no valor do filtro.

## <a name="syntax"></a>Sintaxe

*DataControl*. FilterCriterion = *String*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Um valor **String** que especifica o operador de avaliação do [FilterValue](filtervalue-property-rds.md) para os registros. Pode ser qualquer um dos seguintes: \<, \<=, \>, \>=, =, ou \< \>.|

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion** e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

O "\!=" operador não é válido para **FilterCriterion**; em vez disso, use "\<\>".

Se tanto as propriedades de filtro como as de classificação estiverem definidas, e o método **Reset** for chamado, o conjunto de linhas será filtrado primeiro e depois classificado. Nas classificações em ordem crescente, os valores nulos ficam na parte superior; nas classificações em ordem decrescente, os valores nulos ficam na parte inferior (a ordem crescente é o comportamento padrão).

