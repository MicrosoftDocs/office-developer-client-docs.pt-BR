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
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
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
  
> Ponteiro para uma estrutura [GUID](guid.md) que define um determinado conjunto de propriedades; Este membro não pode ser nulo. Os valores válidos são os seguintes: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Um valor definido pelo cliente
  
> 
    
 **Uikindda**
  
> Valor que descreve o tipo de valor no membro do **tipo** . Os valores válidos são os seguintes: 
    
MNID_ID 
  
> O **tipo** membro contém um valor inteiro que representa o nome da propriedade. 
    
MNID_STRING 
  
> O **tipo** member contém uma cadeia de caracteres Unicode que representa o nome da propriedade. 
    
 **Tipo**
  
> União descrevendo o nome da propriedade nomeada. O nome pode ser um valor inteiro, armazenado em **tampa**ou uma cadeia de caracteres Unicode, armazenado em **lpwstrName**.
    
## <a name="remarks"></a>Comentários

A estrutura **MAPINAMEID** é usada para descrever propriedades nomeadas propriedades que têm identificadores sobre 0x8000. Um conjunto de propriedades é uma parte importante de uma propriedade nomeada. Por exemplo, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE são conjuntos de propriedades definidos por MAPI. 
  
As propriedades nomeadas permitem que os clientes definam Propriedades personalizadas em um namespace maior do que o disponível no intervalo de identificador de propriedade definida por MAPI. Os nomes de propriedade não podem ser usados para obter valores de propriedade diretamente; Eles devem ser mapeados primeiro para os identificadores de propriedade por meio do método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Para determinados objetos como mensagens, MAPI reserva um intervalo de identificadores de propriedade para propriedades personalizadas. Portanto, para esses objetos, os clientes não precisam usar propriedades nomeadas e podem salvar a sobrecarga associada. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [propriedades nomeadas](mapi-named-properties.md).
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Estruturas MAPI](mapi-structures.md)

