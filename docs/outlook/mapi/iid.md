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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411593"
---
# <a name="iid"></a>IID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma estrutura [GUID](guid.md) usada para descrever um identificador de uma interface MAPI. 
  
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

Consulte a estrutura **GUID** . 
  
## <a name="remarks"></a>Comentários

Uma estrutura de **IID** é usada para identificar exclusivamente uma interface MAPI e para associar uma interface específica a um objeto. Por exemplo, quando um cliente chama [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir uma pasta, o cliente define o parâmetro _lpInterface_ para apontar para um **IID** representando a interface [IMAPIFolder](imapifolderimapicontainer.md) . MAPI define o **IMAPIFolderIID** a ser IID_IMAPIFolder. As estruturas de **IID** também são usadas para identificar exclusivamente interfaces OLE. 
  
Todas as estruturas de **IID** específicas para as interfaces MAPI são definidas no arquivo de cabeçalho Mapiguid. h. 
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)


[Estruturas MAPI](mapi-structures.md)

