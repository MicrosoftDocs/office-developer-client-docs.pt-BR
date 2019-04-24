---
title: Método Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309294"
---
# <a name="refresh-method-rds"></a>Método Refresh (RDS)

**Aplica-se ao:** Access 2013, Office 2013

Consulta novamente a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) e atualiza os resultados da consulta.

## <a name="syntax"></a>Sintaxe

*DataControl*. Atualizado

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentários

Você deve definir as propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) antes de utilizar o método **Refresh**. Todos os controles acoplados a dados no formulário associado a um objeto **RDS.DataControl** refletirão o novo conjunto de registros. Qualquer objeto [Recordset](recordset-object-ado.md) pré-existente será liberado e quaisquer alterações não salvas serão descartadas. O método **Refresh** torna automaticamente o primeiro registro o registro atual.

É uma boa ideia chamar o método **Refresh** periodicamente ao trabalhar com dados. Se você recuperar dados e, em seguida, deixá-los na máquina cliente por um tempo, é provável que eles fiquem desatualizados. É possível que quaisquer alterações que você fez falhem, porque alguma outra pessoa pode ter alterado o registro e submetido alterações antes de você.

