---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765267"
---
# <a name="closesession"></a>CloseSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Finaliza uma sessão com um cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parâmetros

_SessionId_
  
> A identificação da sessão para fechar. Este valor deve corresponder o valor retornado pela [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor retornado

**xlHpcRetSuccess** se a sessão é fechada; **xlHpcRetInvalidSessionId** se o argumento _SessionId_ é inválido; **xlHpcRetCallFailed** em outras falhas. 
  
## <a name="see-also"></a>Confira também

- [OpenSession](opensession.md)
- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

