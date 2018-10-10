---
title: Propriedade SortDirection (RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 256e6a878e9c3f382bcd65b9138df7a440bf118c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464717"
---
# <a name="sortdirection-property-rds"></a>Propriedade SortDirection (RDS)


**Aplica-se a**: Access 2013 | Office 2013


Indica se uma ordem de classificação é crescente ou decrescente.

## <a name="syntax"></a>Sintaxe

*DataControl*. SortDirection = *value*

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *Valor*

  - Um valor **Boolean** que, quando definido como **True**, indica a direção da classificação como crescente. **False** indica a ordem decrescente.

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método **Reset** executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

