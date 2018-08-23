---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6b57ed45e067ce2debd40e033d386ad2b5ae895a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568515"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica os status de acompanhamento diferentes para uma mensagem.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a>Members

 _flwupNone_
  
> Nenhum acompanhamento foi especificado.
    
 _flwupComplete_
  
> A mensagem foi concluída.
    
 _flwupMarked_
  
> A mensagem é marcada para acompanhamento.
    
 _flwupMAX_
  
> O número de status diferentes com suporte para acompanhamento.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

