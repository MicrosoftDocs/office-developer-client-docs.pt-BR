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
# <a name="filtervalue-property-rds"></a>Propriedade FilterValue (RDS)


**Aplica-se a**: Access 2013 | Office 2013


Indica o valor com o qual os registros são filtrados.

## <a name="syntax"></a>Sintaxe

*DataControl*. FilterValue = *String*

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *String*

  - Um valor **String** que representa um valor de dados com o qual deseja filtrar registros (por exemplo, 'Programmer' ou 125).

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e filtragem no cache do lado do cliente. A funcionalidade de classificação ordena os registros de acordo com os valores de uma coluna. A funcionalidade de filtragem exibe um subconjunto de registros com base nos critérios de localização, enquanto todo o [Recordset](recordset-object-ado.md) é mantido no cache. O método [Reset](reset-method-rds.md) executará os critérios e substituirá o **Recordset** atual por um **Recordset** que pode ser atualizado.

Valores nulos resultam em um erro de tipos incompatíveis.
