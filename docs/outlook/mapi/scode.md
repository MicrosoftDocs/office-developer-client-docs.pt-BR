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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6cd9dfe8fabd1ae7a4389550c628fb7ceff09ea8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770319"
---
# <a name="scode"></a>SCODE

**Aplica-se a**: Outlook 
  
Um valor de status de 32 bits que é usado para descrever um erro ou aviso. 
  
```cpp
typedef ULONG SCODE;

```

## <a name="remarks"></a>Comentários

O tipo de dados **SCODE** é o mesmo que o tipo de dados [HRESULT](hresult.md) . 
  
Um valor **SCODE** é dividido em quatro campos: 
  
- Um código de gravidade bit único que é definido como 0 para indicar êxito e 1 para indicar falha.
    
- Um campo reservado de 11 bits
    
- Um código de instalações de 4 bits que indica a área responsável pelo erro ou aviso.
    
- Um erro de 16 bits ou código de aviso que descreve o problema que está causando o erro ou aviso.
    
Muitas das funções MAPI e métodos retornam valores **SCODE** definidos como tipos de dados **HRESULT** , assim como as funções e os métodos OLE. OLE define várias macros que podem ser usadas para converter entre um **SCODE** e um **HRESULT**.
  
> [!NOTE]
> Em MAPI de 64 bits, **SCODE** ainda é um valor de 32 bits. 
  
Para obter mais informações sobre como o MAPI usa o tipo de dados **SCODE** , consulte o [Tratamento de erros](error-handling-in-mapi.md). Para obter mais informações sobre o OLE e o tipo de dados **SCODE** , consulte a *referência do programador do OLE* . 
  
## <a name="see-also"></a>Confira também



[HRESULT](hresult.md)


[Tipos de dados MAPI](mapi-data-types.md)

