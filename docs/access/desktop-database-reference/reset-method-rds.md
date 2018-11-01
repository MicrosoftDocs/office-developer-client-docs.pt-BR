---
title: Método Reset (RDS - referência de banco de dados da área de trabalho do Access)
TOCTitle: Reset Method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab88aefabca73b9c2b23a4cf66664aa892310cdc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884482"
---
# <a name="reset-method-rds"></a>Método Reset (RDS)


**Aplica-se a**: Access 2013, o Office 2013

Executa a classificação ou a filtragem em um **Recordset** de cliente, com base nas propriedades de classificação e filtragem especificadas.

## <a name="syntax"></a>Sintaxe

*DataControl*. Redefinição (*valor*)

## <a name="parameters"></a>Parâmetros

  - *DataControl*

  - Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).

  - *value*

  - Opcional. Um valor **Boolean** que é **True** (padrão) se você deseja filtrar pelo conjunto de linhas "filtrado" atual. **False** indica que você filtra pelo conjunto de linhas original, removendo quaisquer opções de filtro anteriores.

## <a name="remarks"></a>Comentários

As propriedades [SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md) e [FilterColumn](filtercolumn-property-rds.md) fornecem funcionalidade de classificação e de filtro no cache do cliente. A funcionalidade de classificação ordena os registros pelos valores de uma coluna. A funcionalidade de filtro exibe um subconjunto de registros com base em critérios de localização, enquanto o [Recordset](recordset-object-ado.md) completo é mantido no cache. O método **Reset** irá executar os critérios e substituir o **Recordset** atual por um **Recordset** atualizável.

Se houver alterações nos dados originais que ainda não foram submetidas, o método **Reset** falhará. Primeiro, utilize o método [SubmitChanges](submitchanges-method-rds.md) para salvar quaisquer alterações em um **Recordset** de leitura/gravação e, em seguida, utilize o método **Reset** para classificar ou filtrar os registros.

Se você quiser executar mais de um filtro no seu conjunto de linhas, você pode usar o opcional argumento *booleano* com o método **Reset** . O exemplo a seguir mostra como fazer isso:

