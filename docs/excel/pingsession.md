---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408359"
---
# <a name="pingsession"></a>PingSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Verifica se uma sessão é válida. Essa função normalmente é chamada quando o Excel precisa determinar se uma ID de sessão anteriormente retornada ainda está ativa e pode ser usada.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parâmetros

_SessionID_
  
> A ID da sessão para o ping. Esse valor deve corresponder a uma ID retornada por uma chamada anterior para [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se o argumento _SessionID_ for válido; caso contrário, **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Confira também

- [OpenSession](opensession.md)
- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

