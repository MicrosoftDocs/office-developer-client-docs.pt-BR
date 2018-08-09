---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765430"
---
# <a name="opensession"></a>OpenSession

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Cria uma sessão em que as funções definidas pelo usuário podem ser executadas.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parâmetros

_Parâmetros_
  
> Um ponteiro para separados por ponto-e-vírgula de cadeia de caracteres UNICODE de parâmetros para a sessão. O Excel não usa este argumento.
    
## <a name="return-value"></a>Valor retornado

Uma identificação de sessão para usar em outras chamadas para o conector de cluster, se a sessão foi criada com êxito; Caso contrário **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

