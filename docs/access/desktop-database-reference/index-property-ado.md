---
title: Propriedade Index (ADO)
TOCTitle: Index property (ADO)
ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15)
ms:contentKeyID: 48544715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d436ec9102c4c75688b6c6ac973ca85e8c280d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291703"
---
# <a name="index-property-ado"></a>Propriedade Index (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o nome do índice que está atualmente em vigor para um objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor **String**, que é o nome do índice.

## <a name="remarks"></a>Comentários

O índice nomeado pela propriedade **Index** deve ter sido declarado anteriormente na tabela de base subjacente ao objeto **Recordset**. Ou seja, o índice deve ter sido declarado de forma programática como um objeto [Index](index-object-adox.md) do ADOX ou quando a tabela de base foi criada.

Um erro de tempo de execução ocorrerá se o índice não puder ser definido. A propriedade **Index** não poderá ser definida:

  - Dentro de um manipulador de eventos [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) ou **RecordsetChangeComplete**.

  - Se o **Recordset** ainda estiver executando uma operação (o que pode ser determinado pela propriedade [State](state-property-ado.md)).

  - Se um filtro tiver sido definido no **Recordset** com a propriedade [Filter](filter-property-ado.md).

A propriedade **Index** sempre poderá ser definida com sucesso se o **Recordset** estiver fechado, mas o **Recordset** não será aberto com sucesso, ou o índice não poderá ser usado, se o provedor de base não oferecer suporte a índices.

Se o índice puder ser definido, a posição da linha atual poderá ser alterada. Isso atualizará a propriedade [AbsolutePosition](absoluteposition-property-ado.md) e a geração dos eventos **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) e [MoveComplete](willmove-and-movecomplete-events-ado.md).

Se o índice puder ser definido e a propriedade [LockType](locktype-property-ado.md) for **adLockPessimistic** ou **adLockOptimistic**, uma operação [UpdateBatch](updatebatch-method-ado.md) implícita será executada. Isso libera os grupos atuais e afetados. Qualquer filtro existente é liberado, e a posição da linha atual é alterada para a primeira linha do **Recordset** reordenado.

A propriedade **Index** é usada em conjunto com o método [Seek](seek-method-ado.md). Se o provedorde base não oferecer suporte à propriedade **Index** e, consequentemente, ao método **Seek**, considere o uso do método [Find](find-method-ado.md). Determine se o **objeto Recordset** oferece suporte a índices com o método [Supports](supports-method-ado.md)**(adIndex).**

A propriedade interna **Index** não está relacionada à propriedade [Optimize](optimize-property-dynamic-ado.md) dinâmica, embora as duas lidem com índices.

