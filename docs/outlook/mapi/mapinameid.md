---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411677"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma propriedade nomeada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>Members

 **lpguid**
  
> Ponteiro para uma [estrutura GUID](guid.md) definindo um conjunto de propriedades específico; este membro não pode ser NULL. Os valores válidos são: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Um valor definido pelo cliente
  
> 
    
 **ulKind**
  
> Valor que descreve o tipo de valor no **membro Kind.** Os valores válidos são os seguinte: 
    
MNID_ID 
  
> O **membro Kind** contém um valor inteiro que representa o nome da propriedade. 
    
MNID_STRING 
  
> O **membro Kind** contém uma cadeia de caracteres Unicode que representa o nome da propriedade. 
    
 **Tipo**
  
> União que descreve o nome da propriedade nomeada. O nome pode ser um valor inteiro, armazenado em **lID** ou uma cadeia de caracteres Unicode, armazenado em **lpwstrName**.
    
## <a name="remarks"></a>Comentários

A **estrutura MAPINAMEID** é usada para descrever propriedades nomeadas com identificadores sobre 0x8000. Um conjunto de propriedades é uma parte importante de uma propriedade nomeada. Por exemplo, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE são conjuntos de propriedades definidos por MAPI. 
  
As propriedades nomeadas permitem que os clientes definam propriedades personalizadas em um namespace maior do que o disponível no intervalo de identificadores de propriedade definidos por MAPI. Os nomes de propriedade não podem ser usados para obter valores de propriedade diretamente; eles devem primeiro ser mapeados para identificadores de propriedade por meio do [método IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Para objetos específicos, como mensagens, o MAPI reserva um intervalo de identificadores de propriedade para propriedades personalizadas. Portanto, para esses objetos, os clientes não têm que usar propriedades nomeadas e podem economizar a sobrecarga associada. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [Propriedades Nomeadas.](mapi-named-properties.md)
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Estruturas MAPI](mapi-structures.md)

