---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767688"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Aplica-se a**: Outlook 
  
Inicia uma sessão de sincronização e obtém a interface **[IOSTX](iostxiunknown.md)** associada. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Par�metros

 _ppostx_
  
>  [out] Ponteiro para a interface **IOSTX** a ser obtido. 
    
## <a name="remarks"></a>Coment�rios

O chamador deve assegurar que a mesma pasta não está sincronizada ao mesmo tempo em mais de um segmento.
  
## <a name="see-also"></a>Confira também



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

