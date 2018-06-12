---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767297"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Aplica-se a**: Outlook 
  
Atualiza o status na caixa de diálogo Enviar/receber. O provedor de armazenamento periodicamente chama essa função.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Par�metros

 **pwczsProgress**
  
> Um ponteiro para uma cadeia de caracteres que exibe a etapa de andamento atual. Pode ser NULL para atualizar progresso.
    
 **ulIndex**
  
> A posição atual em andamento.
    
 **ulIndexMax**
  
> O índice que indica o progresso completo.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)

