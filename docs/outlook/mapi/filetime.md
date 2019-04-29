---
title: FILETIME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FILETIME
api_type:
- COM
ms.assetid: 4af8e79a-697e-44a1-8576-fdc57726e9ef
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00355546717ca61492750cb1dd113d20114b0695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409500"
---
# <a name="filetime"></a>FILETIME

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de data e hora de 64 bits não assinados para um arquivo. Esse valor representa o número de unidades de 100-nanossegundos desde o início de 1º de janeiro de 1601. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Bits de 32 de ordem inferior do valor de tempo do arquivo. 
    
 **dwHighDateTime**
  
> Alta ordem 32 bits do valor de tempo do arquivo.
    
## <a name="remarks"></a>Comentários

Uma propriedade do tipo PT_SYSTIME tem uma estrutura **FILETIME** para o valor. Tal propriedade tem um tipo de dados **FILETIME** para o membro **Value** em sua definição em uma estrutura [SPropValue](spropvalue.md) . 
  
A definição da estrutura **FILETIME** está na _referência do programador do Win32_ e no arquivo de cabeçalho MAPI mapidefs. h. MAPI define a estrutura condicionalmente para garantir que ela seja definida quando a definição do Win32 não estiver disponível. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

