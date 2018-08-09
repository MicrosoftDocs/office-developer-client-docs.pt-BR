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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767990"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**Aplica-se a**: Outlook 
  
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
  
> Ponteiro para uma estrutura [GUID](guid.md) definindo uma determinada propriedade definido; Este membro não pode ser NULL. Os valores válidos são: 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Um valor definido pelo cliente
  
> 
    
 **ulKind**
  
> Descrevendo o tipo de valor no membro do **tipo** de valor. Os valores válidos são: 
    
MNID_ID 
  
> O **tipo** de membro contém um valor integer que representa o nome da propriedade. 
    
MNID_STRING 
  
> O **tipo** de membro contém uma cadeia de caracteres Unicode que representa o nome da propriedade. 
    
 **Tipo**
  
> União descrevendo o nome da propriedade nomeada. O nome pode ser um valor inteiro, armazenados em **lID**, ou uma cadeia de caracteres Unicode, armazenado em **lpwstrName**.
    
## <a name="remarks"></a>Comentários

A estrutura **MAPINAMEID** é usada para descrever as propriedades de propriedades nomeadas que têm identificadores 0x8000 acima. Um conjunto de propriedades é uma parte importante de uma propriedade nomeada. Por exemplo, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE são conjuntos de propriedades definidos pelo MAPI. 
  
Propriedades nomeadas permitem que os clientes definir propriedades personalizadas em um namespace maior que o disponíveis no intervalo de identificador de propriedade definida pelo MAPI. Os nomes de propriedade não podem ser usados para obter valores de propriedade diretamente; eles primeiro devem ser mapeados para os identificadores de propriedade por meio do método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Para objetos específicos, como mensagens, MAPI reserva um intervalo de identificadores de propriedade de propriedades personalizadas. Portanto, para esses objetos, clientes não precisam usar propriedades nomeadas e pode salvar o associado sobrecarga. 
  
Para obter mais informações sobre propriedades nomeadas, consulte [Propriedades chamado](mapi-named-properties.md).
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Estruturas MAPI](mapi-structures.md)

