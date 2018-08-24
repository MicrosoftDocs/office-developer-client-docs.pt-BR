---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9f09f29d67bff6588c826b92d93aead491510cef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574815"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o contexto de modo de exibição atual para o formulário. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parâmetros

 _ppViewContext_
  
> [out] Um ponteiro para um ponteiro para o contexto de exibição do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Contexto de modo de exibição atual do formulário foi retornado com êxito. 
    
S_FALSE 
  
> Não há nenhum contexto de modo de exibição para o formulário.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame **GetViewContext** para obter um ponteiro para o contexto de modo de exibição estabelecido em uma chamada anterior para [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Se nenhuma chamada anterior foi feita para **SetViewContext**, **GetViewContext** define _ppViewContext_ como NULL. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Copie o ponteiro de contexto do modo de exibição do formulário para o ponteiro transmitido pelo Visualizador formulário chamada no parâmetro _ppViewContext_ . Se o formulário não terá um contexto de modo de exibição, defina _ppViewContext_ como NULL. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o método **IMAPIForm::GetViewContext** para verificar se um formulário tem um contexto de modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

