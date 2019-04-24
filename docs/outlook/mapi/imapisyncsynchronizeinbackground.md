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
description: 'Última modificação: 26 de junho de 2012'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341367"
---
# <a name="imapisync--synchronizeinbackground"></a>IMAPISync : SynchronizeInBackground

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Inicia uma sincronização. Este método é chamado pelo Microsoft Outlook 2010 e pelo Microsoft Outlook 2013 e implementado por provedores de repositório de mensagens. 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a>Parâmetros

 _psibpb_
  
> Informa ao provedor sobre o que será sincronizado e fornece acesso a interfaces que podem ser usadas durante a sincronização. É uma estrutura [MAPISIB](mapisib.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="see-also"></a>Confira também



[IMAPISync : IUnknown](imapisynciunknown.md)
  
[MAPISIB](mapisib.md)

