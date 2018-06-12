---
title: IMAPISync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: 'Modificado pela última vez: 26 de junho de 2012'
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767311"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync: SynchronizeInBackground

 
  
**Aplica-se a**: Outlook 
  
 Inicia uma sincronização. Esse método é chamado pelo Microsoft Outlook 2010 e o Microsoft Outlook 2013 e implementado por provedores de armazenamento de mensagem. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Par�metros

 _psibpb_
  
> Informa o provedor do qual será sincronizado e fornece acesso a interfaces que podem ser usadas durante a sincronização. Ele é uma estrutura [MAPISIB](mapisib.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISync: IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

