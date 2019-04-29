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
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418705"
---
# <a name="mapisib"></a>MAPISIB

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Essa estrutura é usada com [IMAPISync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).
  
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
  
> Um sinalizador que indica o tipo de sincronização. Deve ser um dos seguintes valores:
    
||||
|:-----|:-----|:-----|
|SYNC_OUTGOING_MAIL  <br/> |0x00000200  <br/> |Envie a mensagem para o servidor (não está em uso no momento).  <br/> |
|SYNC_UPLOAD_HIERARCHY  <br/> |0x00000001  <br/> |Push as alterações de hierarquia para o servidor.  <br/> |
|SYNC_DOWNLOAD_HIERARCHY  <br/> |0x00000002  <br/> |Extrair alterações de hierarquia do servidor.  <br/> |
|SYNC_UPLOAD_CONTENTS  <br/> |0x00000040  <br/> |Alterações de mensagens por push no servidor.  <br/> |
|SYNC_DOWNLOAD_CONTENTS  <br/> |0x00000080  <br/> |As alterações de mensagem de recebimento do servidor.  <br/> |
|SYNC_ON_DEMAND  <br/> |0x20000000  <br/> |A sincronização foi iniciada pelo usuário e deve ser uma prioridade mais alta.  <br/> |
|SYNC_GLOBAL_HEADERS  <br/> |0x02000000  <br/> |Só deve sincronizar cabeçalhos e não corpos completos.  <br/> |
   
 **psesSync**
  
> NO Um ponteiro para a sessão MAPI.
    
 **punkCallBack**
  
> NO Um ponteiro para a interface na qual fornecer progresso. Ele pode ser usado para consultar a interface para [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md).
    
 **\*phSyncDoneEvent**
  
> BOTA O evento que ocorrerá quando o thread que acabou de ser criado estiver concluído. O ponteiro deve ser válido, pois conterá o evento.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)
  
[IMAPISync : IUnknown](imapisynciunknown.md)

