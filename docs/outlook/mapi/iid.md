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
ms.openlocfilehash: 00c7560427ece58026030ce6895d60aec7cc5a2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570937"
---
# <a name="iid"></a>IID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

