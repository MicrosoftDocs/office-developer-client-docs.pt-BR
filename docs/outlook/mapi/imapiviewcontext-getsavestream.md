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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351118"
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
  
> bota Ponteiro para uma bitmask de sinalizadores que controla como o texto da mensagem deve ser salvo. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O texto da mensagem é salvo no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o texto será salvo no formato ANSI.
    
 _pulFormat_
  
> bota Ponteiro para uma bitmask de sinalizadores que controla o formato do texto salvo. Os seguintes sinalizadores podem ser definidos:
    
SAVE_FORMAT_RICHTEXT 
  
> O texto da mensagem deve ser salvo como texto formatado no formato Rich Text (RTF). 
    
SAVE_FORMAT_TEXT 
  
> O texto da mensagem deve ser salvo como texto sem formatação. 
    
 _ppStm_
  
> bota Ponteiro para um ponteiro para o Stream que conterá a mensagem salva.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O fluxo foi recuperado com êxito.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIViewContext:: GetSaveStream** para recuperar um objeto Stream que implementa a interface **IStream** para suportar o tratamento do verbo salvar como no Visualizador de formulários. O método [IMAPIForm::D overb](imapiform-doverb.md) , que é implementado no servidor de formulário e chamado pelo Visualizador de formulários para invocar um verbo, não deve ser retornado até que a mensagem seja totalmente convertida no formato de texto apropriado e colocado no fluxo apropriado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não grave no fluxo apontado pelo _ppStm_ antes de chamar **GetSaveStream**. Quando **GetSaveStream** retorna, não redefine a posição do ponteiro de busca. Esse ponteiro deve permanecer no final do texto da mensagem salva. 
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

