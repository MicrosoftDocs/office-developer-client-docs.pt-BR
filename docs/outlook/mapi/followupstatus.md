---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418327"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica os diferentes status de acompanhamento de uma mensagem.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Membros

 _flwupNone_
  
> Nenhum acompanhamento foi especificado.
    
 _flwupComplete_
  
> A mensagem foi concluída.
    
 _flwupMarked_
  
> A mensagem está marcada para acompanhamento.
    
 _flwupMAX_
  
> O número de status diferentes com suporte para acompanhamento.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

