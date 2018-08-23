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
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585448"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicia uma sessão de sincronização e obtém a interface **[IOSTX](iostxiunknown.md)** associada. 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>Parâmetros

 _ppostx_
  
>  [out] Ponteiro para a interface **IOSTX** a ser obtido. 
    
## <a name="remarks"></a>Comentários

O chamador deve assegurar que a mesma pasta não está sincronizada ao mesmo tempo em mais de um segmento.
  
## <a name="see-also"></a>Confira também



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

