---
title: Propriedade SortColumn (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 85f2b031ac105bf900548e90eda6c0feb4b78f96
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464220"
---
# <a name="sortcolumn-property-rds"></a>Propriedade SortColumn (RDS)


**Aplica-se a**: Access 2013 | Office 2013

Indica por qual coluna os registros serão classificados.

## <a name="syntax"></a>Sintaxe

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *String*

  - Um valor **String** que representa o nome ou o alias da coluna pela qual os registros serão classificados.

## <a name="remarks"></a>Comentários

As propriedades **SortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

Para classificar em um **Recordset**, você deverá primeiramente salvar quaisquer alterações pendentes. Se você estiver utilizando o **RDS.DataControl**, será possível utilizar o método [SubmitChanges](submitchanges-method-rds.md). Por exemplo, se sua **RDS. DataControl** é denominado ADC1, seu código seria ADC1. SubmitChanges. Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md). O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md). Por exemplo, seu código poderia ser myRS.UpdateBatch ou. Se estiver utilizando um **Recordset** do ADO, você poderá utilizar seu método [UpdateBatch](updatebatch-method-ado.md). O uso do **UpdateBatch** é o método recomendado para os objetos **Recordset** criados com o método [CreateRecordset](createrecordset-method-rds.md). Por exemplo, seu código poderia ser myRS.UpdateBatch ou ADC1. Recordset.UpdateBatch.

