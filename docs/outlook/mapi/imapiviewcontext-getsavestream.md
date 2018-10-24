---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 47ea122fce7969b326dbd48f875696b91de464f5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568571"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera um fluxo a ser usado para salvar a mensagem atual.
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>Parâmetros

 _pulFlags_
  
> [out] Ponteiro para uma bitmask dos sinalizadores que controla como o texto da mensagem deve ser salvo. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O texto da mensagem é salvo no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o texto é salvo no formato ANSI.
    
 _pulFormat_
  
> [out] Ponteiro para uma bitmask dos sinalizadores que controla o formato do texto salvo. Sinalizadores a seguir podem ser definidos:
    
SAVE_FORMAT_RICHTEXT 
  
> O texto da mensagem deve ser salva como texto formatado em Rich Text Format (RTF). 
    
SAVE_FORMAT_TEXT 
  
> O texto da mensagem deve ser salva como texto sem formatação. 
    
 _ppstm_
  
> [out] Ponteiro para um ponteiro para o fluxo que conterá a mensagem salva.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O fluxo foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método **IMAPIViewContext::GetSaveStream** para recuperar um fluxo de um objeto que implementa a interface **IStream** para oferecer suporte a manipulação do verbo Salvar como no Visualizador do formulário. O método [IMAPIForm::DoVerb](imapiform-doverb.md) , que é implementado no servidor de formulário e chamado pelo Visualizador do formulário para chamar um verbo, não deve retornar até que a mensagem é totalmente convertida em formato de texto apropriado e colocada no stream apropriado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não grava no fluxo apontado pela _ppstm_ antes de chamar **GetSaveStream**. Quando **GetSaveStream** retorna, não redefina a posição do ponteiro do seek. Esse ponteiro deve permanecer no final do texto da mensagem salva. 
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

