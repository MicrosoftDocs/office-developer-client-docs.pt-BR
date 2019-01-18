---
title: Evento WillExecute (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7fe15604d0160afcbde5fdf02eaa6a7831da874b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718564"
---
# <a name="willexecute-event-ado"></a>Evento WillExecute (ADO)

**Aplica-se a**: Access 2013, o Office 2013

O evento **WillExecute** é chamado um pouco antes da execução de um comando pendente, em uma conexão.

## <a name="syntax"></a>Sintaxe

WillExecute*Source*, *CursorType*, *LockType*, *Opções*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Uma **sequência de caracteres** que contém um comando SQL ou um nome de procedimento armazenado.|
|*CursorType* |Um [CursorTypeEnum](cursortypeenum.md) que contém o tipo de cursor para o **Recordset** que será aberto. Com esse parâmetro, você pode alterar o cursor para qualquer tipo durante uma operação de [abertura](open-method-ado-recordset.md) do **Recordset** . Para qualquer outra operação *CursorType* será ignorada.|
|*LockType* |Um [LockTypeEnum](locktypeenum.md) que contém o tipo de bloqueio para o **Recordset** que será aberto. Com esse parâmetro, você pode alterar o bloqueio para qualquer tipo, durante a operação **Open** do **Recordset**. Para qualquer outra operação *LockType* será ignorada.|
|*Options* |Um valor **Long** que indica as opções que podem ser usadas para executar o comando ou abrir o **Recordset**.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Antes que esse evento retorne, defina esse parâmetro como **adStatusUnwantedEvent**, para evitar notificações subsequentes, ou como **adStatusCancel** para solicitar o cancelamento da operação que gerou esse evento.|
|*pCommand* |O objeto [Command](command-object-ado.md) ao qual essa notificação de evento se aplica.|
|*pRecordset* |O objeto [Recordset](recordset-object-ado.md) ao qual essa notificação de evento se aplica.|
|*pConnection* |O objeto [Connection](connection-object-ado.md) ao qual essa notificação de evento se aplica.|

## <a name="remarks"></a>Comentários

Um evento **WillExecute** pode ocorrer devido a um **Conexão.** [Executar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **comando.** [Executar](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), ou **Recordset.** O parâmetro *pConnection* do método [Open](open-method-ado-recordset.md) sempre deve conter uma referência válida a um objeto de **Conexão** . Se o evento for devido à **Connection. Execute**, os parâmetros *pRecordset* e *pCommand* são definidos como **Nothing**. Se o evento for devido ao **Recordset**, o parâmetro *pRecordset* fará referência do objeto **Recordset** e o parâmetro *pCommand* é definido como **Nothing**. Se o evento for devido à **Command. Execute**, o parâmetro *pCommand* fará referência o objeto **Command** e o parâmetro *pRecordset* é definido como **Nothing**.

**WillExecute** permite examinar e modificar os parâmetros de execução pendentes. Esse evento pode retornar uma solicitação para que o comando pendente seja cancelado.

