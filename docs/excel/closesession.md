---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304134"
---
# <a name="closesession"></a>CloseSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Finaliza uma sessão com um cluster.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Parâmetros

_Identificação_da_sessão_
  
> A ID da sessão a ser fechada. Esse valor deve corresponder ao valor retornado por [OpenSession](opensession.md).
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se a sessão foi fechada; **xlHpcRetInvalidSessionId** se o argumento _SessionID_ for inválido; **xlHpcRetCallFailed** em outras falhas. 
  
## <a name="see-also"></a>Confira também

- [OpenSession](opensession.md)
- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

