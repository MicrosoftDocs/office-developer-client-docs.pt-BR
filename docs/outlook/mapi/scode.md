---
title: SCODE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: 2348cce1-07c3-49ed-ae03-79e477d3c6c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4208f51af44055b03c65b51c9b3d94e947dc9b68
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351237"
---
# <a name="scode"></a>SCODE

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um valor de status de 32 bits usado para descrever um erro ou aviso. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Comentários

O tipo de dados **SCODE** é o mesmo que o tipo de dados [HRESULT](hresult.md) . 
  
Um valor **SCODE** é dividido em quatro campos: 
  
- Um código de severidade de bit único que é definido como 0 para indicar êxito e 1 para indicar falha.
    
- Um campo reservado de 11 bits
    
- Um código de recurso de 4 bits que indica a área responsável pelo erro ou aviso.
    
- Um erro de 16 bits ou um código de aviso que descreve o problema que está causando o erro ou aviso.
    
Muitos dos métodos e funções MAPI retornam valores de **SCODE** definidos como tipos de dados **HRESULT** como os métodos e funções OLE. O OLE define várias macros que podem ser usadas para converter entre um **SCODE** e um **HRESULT**.
  
> [!NOTE]
> No MAPI de 64 bits, **SCODE** ainda é um valor de 32 bits. 
  
Para saber mais sobre como o MAPI usa o tipo de dados **SCODE** , confira [tratamento de erros](error-handling-in-mapi.md). Para obter mais informações sobre OLE e o tipo de dados **SCODE** , consulte a *referência do programador de OLE* . 
  
## <a name="see-also"></a>Confira também



[HRESULT](hresult.md)


[Tipos de dados MAPI](mapi-data-types.md)

