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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341255"
---
# <a name="imapisyncprogresscallbackprogress"></a>IMAPISyncProgressCallback::Progress

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Atualiza o status na caixa de diálogo enviar/receber. O provedor de repositórios chama periodicamente essa função.
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a>Parâmetros

 **pwczsProgress**
  
> Um ponteiro para uma cadeia de caracteres que exibe a etapa de progresso atual. Pode ser nulo para atualizar o andamento.
    
 **ulIndex**
  
> A posição atual em andamento.
    
 **ulIndexMax**
  
> O índice que indica o progresso completo.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

