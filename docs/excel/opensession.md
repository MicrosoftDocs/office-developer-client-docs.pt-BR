---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301628"
---
# <a name="opensession"></a>OpenSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Cria uma sessão na qual as funções definidas pelo usuário podem ser executadas.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parâmetros

_Parâmetros_
  
> Um ponteiro para a cadeia de caracteres UNICODE delimitada por ponto-e-vírgula de parâmetros da sessão. O Excel não usa esse argumento.
    
## <a name="return-value"></a>Valor de retorno

Uma ID de sessão para usar em outras chamadas para o conector de cluster, se a sessão foi criada com êxito; caso contrário, **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

