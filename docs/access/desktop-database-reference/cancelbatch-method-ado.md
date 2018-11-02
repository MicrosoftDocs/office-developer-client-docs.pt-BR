---
title: Método CancelBatch (ADO)
TOCTitle: CancelBatch method (ADO)
ms:assetid: be7bf073-ed0b-e24c-7ec0-b7379236782a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249925(v=office.15)
ms:contentKeyID: 48547463
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eefe1042404c24040aef204a1ceca0ce583847e8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926952"
---
# <a name="cancelbatch-method-ado"></a>Método CancelBatch (ADO)


**Aplica-se a**: Access 2013, o Office 2013


Cancela uma atualização em lotes pendente.

## <a name="syntax"></a>Sintaxe

*conjunto de registros*. CancelBatch *AffectRecords*

## <a name="parameters"></a>Parâmetros

  - *AffectRecords*

  - Opcional. Um valor [AffectEnum](affectenum.md) que determina a quantidade de registros que serão afetados pelo método **CancelBatch**.

## <a name="remarks"></a>Comentários

Use o método **CancelBatch** para cancelar todas as atualizações pendentes em um [Recordset](recordset-object-ado.md) no modo de atualização em lotes. Se **Recordset** estiver no modo de atualização imediata, um erro será gerado se **CancelBatch** for chamado sem **adAffectCurrent**.

Se você estiver editando o registro atual ou adicionando um novo registro ao chamar **CancelBatch**, o ADO chamará primeiro o método [CancelUpdate](cancelupdate-method-ado.md) para cancelar todas as alterações armazenadas em cache. Em seguida, todas as alterações pendentes serão canceladas no **Recordset**.

É possível que o registro atual não possa ser determinado após uma chamada de **CancelBatch**, principalmente se você estiver no processo de adição de um novo registro. Por esse motivo, convém definir a posição do registro atual para um local conhecido no **Recordset** após a chamada de **CancelBatch**. Por exemplo, chame o método [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).

Se a tentativa de cancelar as atualizações pendentes falhar devido a um conflito com os dados subjacentes (por exemplo, por causa da exclusão de um registro por outro usuário), o provedor retornará avisos à coleção [Errors](errors-collection-ado.md), mas não interromperá a execução do programa. Um erro em tempo de execução somente ocorrerá em caso de conflito em todos os registros solicitados. Use a propriedade [Filter](filter-property-ado.md) (**adFilterConflictingRecords**) e a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.

