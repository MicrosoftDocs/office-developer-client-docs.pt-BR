---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765443"
---
# <a name="pingsession"></a>PingSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Verifica se a uma sessão é válida. Essa função geralmente é chamada quando o Excel precisa para determinar se uma identificação de sessão retornadas anteriormente ainda está ativa e pode ser usada.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Par�metros

_SessionID_
  
> A identificação da sessão de ping. Este valor deve corresponder a uma ID retornada por uma chamada anterior para [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor retornado

**xlHpcRetSuccess** se o argumento _SessionId_ é válido. Caso contrário **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>Confira também

- [OpenSession](opensession.md)
- [Funções de conector de Cluster do Excel](excel-cluster-connector-functions.md)

