---
title: Propriedade Prompt -- Dinâmica (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb858186942ac026cbf3e1020c4ac658537093a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465447"
---
# <a name="prompt-property--dynamic-ado"></a>Propriedade Prompt -- Dinâmica (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica se o provedor OLE DB deveria solicitar ao usuário as informações de inicialização.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define e retorna um valor [ConnectPromptEnum](connectpromptenum.md).

## <a name="remarks"></a>Comentários

**Prompt** é uma propriedade dinâmica que pode ser acrescentada à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md) pelo provedor OLE DB. Para solicitar informações de inicialização, normalmente, os provedores OLE DB exibem uma caixa de diálogo para o usuário.

As propriedades dinâmicas de um objeto [Connection](connection-object-ado.md) são perdidas quando **Connection** é fechado. A propriedade **Prompt** deve ser redefinida antes de reabrir o objeto **Connection** para usar um valor diferente do padrão.


> [!NOTE]
> <P>[!OBSERVAçãO] Não especifique que o provedor solicite o usuário em cenários nos quais este não será capaz de responder à caixa de diálogo. Por exemplo, o usuário não será capaz de responder se o aplicativo estiver sendo executado em um sistema de servidor, e não no cliente do usuário, ou se o aplicativo estiver sendo executado em um sistema em que não haja nenhum usuário conectado. Nesses casos, o aplicativo esperará indefinidamente por uma resposta e parecerá que está travado.</P>



**Uso**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
