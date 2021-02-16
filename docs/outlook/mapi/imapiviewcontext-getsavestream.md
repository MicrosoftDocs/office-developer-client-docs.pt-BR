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
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408422"
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

 _lagFlags_
  
> [out] Ponteiro para uma máscara de bits de sinalizadores que controla como o texto da mensagem deve ser salvo. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> O texto da mensagem é salvo no formato Unicode. Se o MAPI_UNICODE não estiver definido, o texto será salvo no formato ANSI.
    
 _milaFormat_
  
> [out] Ponteiro para uma máscara de bits de sinalizadores que controla o formato do texto salvo. Os sinalizadores a seguir podem ser definidos:
    
SAVE_FORMAT_RICHTEXT 
  
> O texto da mensagem deve ser salvo como texto formatado no formato Rich Text (RTF). 
    
SAVE_FORMAT_TEXT 
  
> O texto da mensagem deve ser salvo como texto sem texto simples. 
    
 _ppstm_
  
> [out] Ponteiro para um ponteiro para o fluxo que conterá a mensagem salva.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O fluxo foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chamam o método **IMAPIViewContext::GetSaveStream** para recuperar um fluxo de um objeto que implementa a interface **IStream** para suportar a manipulação do verbo Salvar como no visualizador de formulário. O método [IMAPIForm::D oVerb,](imapiform-doverb.md) que é implementado no servidor de formulário e chamado pelo visualizador de formulário para invocar um verbo, não deve retornar até que a mensagem seja totalmente convertida no formato de texto apropriado e colocada no fluxo apropriado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não escreva no fluxo apontado pelo  _ppstm_ antes de chamar **GetSaveStream**. Quando **GetSaveStream** retornar, não redefinir a posição do ponteiro de busca. Este ponteiro deve permanecer no final do texto da mensagem salva. 
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

