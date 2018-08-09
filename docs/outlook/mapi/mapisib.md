---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8044eb6647e6f437c87bb4d8b021c62ea15f606
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768016"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Aplica-se a**: Outlook 
  
Essa estrutura é usada com [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a>Members

 **ulSize**
  
> O tamanho da estrutura.
    
 **ulFlags**
  
> Um sinalizador que indica o tipo de sincronização. Ele deve ser um dos seguintes valores:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Envie a mensagem para o servidor (não está atualmente em uso).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Hierarquia de push altera para o servidor.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Retire as alterações de hierarquia do servidor.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Enviar mensagem for alterado para o servidor.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |Receba a mensagem é alterado do servidor.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |A sincronização foi iniciada pelo usuário e deve ser uma prioridade mais alta.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Só deve sincronizar cabeçalhos e corpos não está cheio.  <br/> |
   
 **psesSync**
  
> [IN] Um ponteiro para a sessão MAPI.
    
 **punkCallBack**
  
> [IN] Um ponteiro para a interface no qual você deseja fornecer o progresso. Ele pode ser usado para consultar a interface para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> [OUT] O evento que ocorrerá quando o segmento que acabou de ser criado for concluído. O ponteiro deve ser válido, pois ele conterá o evento.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)
