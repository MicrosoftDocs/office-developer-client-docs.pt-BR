---
title: Propriedade SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306885"
---
# <a name="sortcolumn-property-rds"></a>Propriedade SortColumn (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Indica por qual coluna os registros serão classificados.

## <a name="syntax"></a>Sintaxe

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*String* |Um valor **String** que representa o nome ou o alias da coluna pela qual os registros serão classificados.|

## <a name="remarks"></a>Comentários

As propriedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

Para classificar em um **Recordset**, você deverá primeiramente salvar quaisquer alterações pendentes. Se você estiver utilizando o **RDS.DataControl**, será possível utilizar o método [SubmitChanges](submitchanges-method-rds.md). Por exemplo, se seu **RDS. DataControl** é chamado de ADC1, seu código seria ADC1. SubmitChanges . Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md). O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md). Por exemplo, seu código pode ser myRS.UpdateBatch ou . Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md). O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md). Por exemplo, seu código pode ser myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch .

