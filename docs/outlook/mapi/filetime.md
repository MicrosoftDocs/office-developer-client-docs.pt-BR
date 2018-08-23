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
ms.openlocfilehash: d58a216a41ff8fe93387ce6d9d1d6aa16f36f224
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583250"
---
# <a name="filetime"></a>FILETIME

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma data de 64 bits não assinada e o valor de tempo para um arquivo. Esse valor representa o número de unidades de 100 nanossegundos, desde o início do dia 1 de janeiro de 1601. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _FILETIME
{
  DWORD dwLowDateTime;
  DWORD dwHighDateTime;
} FILETIME, FAR *LPFILETIME;

```

## <a name="members"></a>Members

 **dwLowDateTime**
  
> Valor de tempo de 32 bits de ordem baixa do arquivo. 
    
 **dwHighDateTime**
  
> Valor de tempo de 32 bits de ordem alta do arquivo.
    
## <a name="remarks"></a>Comentários

Uma propriedade do tipo PT_SYSTIME tem uma estrutura **FILETIME** para seu valor. Essa propriedade tem um tipo de dados **FILETIME** para o membro de **valor** em sua definição em uma estrutura [SPropValue](spropvalue.md) . 
  
A definição da estrutura **FILETIME** está na _referência do programador do Win32_ e no arquivo de cabeçalho de MAPI Mapidefs.h. MAPI define a estrutura condicionalmente para certificar-se de que ela é definida quando a definição de Win32 não estiver disponível. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

