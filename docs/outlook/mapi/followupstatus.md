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
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766576"
---
# <a name="followupstatus"></a>FollowUpStatus

  
  
**Aplica-se a**: Outlook 
  
Especifica os status de acompanhamento diferentes para uma mensagem.
  
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
  
> A mensagem é marcada para acompanhamento.
    
 _flwupMAX_
  
> O número de status diferentes com suporte para acompanhamento.
    
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagFlagStatus](pidtagflagstatus-canonical-property.md)

