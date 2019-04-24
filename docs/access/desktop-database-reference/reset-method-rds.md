---
title: Método Reset (referência do banco de dados de área de trabalho do Access)
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
# <a name="reset-method-rds"></a>Método Reset (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Executa a classificação ou a filtragem em um **Recordset** de cliente, com base nas propriedades de classificação e filtragem especificadas.

## <a name="syntax"></a>Sintaxe

*DataControl*. Redefinir (*valor*)

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|
|*value* |Opcional. Um valor **Boolean** que é **True** (padrão) se você deseja filtrar pelo conjunto de linhas "filtrado" atual. **False** indica que você filtra pelo conjunto de linhas original, removendo quaisquer opções de filtro anteriores.|

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e de filtro no cache do cliente. A funcionalidade de classificação ordena os registros pelos valores de uma coluna. A funcionalidade de filtro exibe um subconjunto de registros com base em critérios de localização, enquanto o [Recordset](recordset-object-ado.md) completo é mantido no cache. O método **Reset** irá executar os critérios e substituir o **Recordset** atual por um **Recordset** atualizável.

Se houver alterações nos dados originais que ainda não foram submetidas, o método **Reset** falhará. Primeiro, utilize o método [SubmitChanges](submitchanges-method-rds.md) para salvar quaisquer alterações em um **Recordset** de leitura/gravação e, em seguida, utilize o método **Reset** para classificar ou filtrar os registros.

Se você deseja executar mais de um filtro em seu conjunto de linhas, poderá utilizar o argumento opcional *Boolean* com o método **Reset**. O exemplo a seguir mostra como fazer isso:

