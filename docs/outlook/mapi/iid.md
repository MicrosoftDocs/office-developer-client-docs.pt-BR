---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a0e859ac0f8bcc3bd83e336c85da21f1251efcb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766926"
---
# <a name="iid"></a>IID

  
  
**Aplica-se a**: Outlook 
  
Descreve uma estrutura [GUID](guid.md) usada para descrever um identificador para uma interface MAPI. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

Ver a estrutura **GUID** . 
  
## <a name="remarks"></a>Comentários

Uma estrutura **IID** é usada para identificar exclusivamente uma interface MAPI e para associar a um objeto de uma determinada interface. Por exemplo, quando um cliente chamadas [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir uma pasta, o cliente define o parâmetro _lpInterface_ para apontar para um **IID** representando a interface [IMAPIFolder](imapifolderimapicontainer.md) . MAPI define o **IMAPIFolderIID** para ser IID_IMAPIFolder. Estruturas **IID** também são usadas para identificar exclusivamente interfaces OLE. 
  
Todas as estruturas **IID** específicas para as interfaces de MAPI são definidas no arquivo de cabeçalho Mapiguid.h. 
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)


[Estruturas MAPI](mapi-structures.md)

