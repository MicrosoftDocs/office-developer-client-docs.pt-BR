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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a5f950907e2b14cb4101a094715c24b25beb2016
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766555"
---
# <a name="filetime"></a>FILETIME

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="members"></a>Membros

 **dwLowDateTime**
  
> Valor de tempo de 32 bits de ordem baixa do arquivo. 
    
 **dwHighDateTime**
  
> Valor de tempo de 32 bits de ordem alta do arquivo.
    
## <a name="remarks"></a>Coment�rios

Uma propriedade do tipo PT_SYSTIME tem uma estrutura **FILETIME** para seu valor. Essa propriedade tem um tipo de dados **FILETIME** para o membro de **valor** em sua definição em uma estrutura [SPropValue](spropvalue.md) . 
  
A definição da estrutura **FILETIME** está na _referência do programador do Win32_ e no arquivo de cabeçalho de MAPI Mapidefs.h. MAPI define a estrutura condicionalmente para certificar-se de que ela é definida quando a definição de Win32 não estiver disponível. 
  
## <a name="see-also"></a>Confira também



[SPropValue](spropvalue.md)


[Estruturas MAPI](mapi-structures.md)

