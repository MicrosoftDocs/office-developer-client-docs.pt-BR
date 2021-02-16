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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407106"
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
  
>  [out] Ponteiro para a interface **IOSTX** a ser obter. 
    
## <a name="remarks"></a>Comentários

O chamador deve garantir que a mesma pasta não seja sincronizada ao mesmo tempo em mais de um thread.
  
## <a name="see-also"></a>Confira também



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

