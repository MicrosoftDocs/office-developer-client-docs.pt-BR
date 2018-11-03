---
title: Método Refresh (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49b91f129a0661c5c81243bb405de9088b1e06d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950115"
---
# <a name="refresh-method-rds"></a>Método Refresh (RDS)

**Aplica-se a**: Access 2013, o Office 2013

Consulta novamente a fonte de dados especificada na propriedade [Connect](connect-property-rds.md) e atualiza os resultados da consulta.

## <a name="syntax"></a>Sintaxe

*DataControl*. Atualizar

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*DataControl* |Uma variável de objeto que representa um objeto [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Comentários

Você deve definir as propriedades [Connect](connect-property-rds.md), [Server](server-property-rds.md) e [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) antes de utilizar o método **Refresh**. Todos os controles acoplados a dados no formulário associado a um objeto **RDS.DataControl** refletirão o novo conjunto de registros. Qualquer objeto [Recordset](recordset-object-ado.md) pré-existente será liberado e quaisquer alterações não salvas serão descartadas. O método **Refresh** torna automaticamente o primeiro registro o registro atual.

É uma boa ideia chamar o método **Refresh** periodicamente ao trabalhar com dados. Se você recuperar dados e, em seguida, deixá-los na máquina cliente por um tempo, é provável que eles fiquem desatualizados. É possível que quaisquer alterações que você fez falhem, porque alguma outra pessoa pode ter alterado o registro e submetido alterações antes de você.

