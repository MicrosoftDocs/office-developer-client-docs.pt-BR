---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 26ca126603ac1e695bd14a10cd8d9e637382b2e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584300"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece um contexto de modo de exibição para o formulário. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Parâmetros

 _pViewContext_
  
> [in] Um ponteiro para o novo contexto de modo de exibição para o formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O contexto de modo de exibição foi definido com êxito.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIForm::SetViewContext** para estabelecer um contexto de modo de exibição de formulário específico como o atual. Um formulário pode ter apenas um contexto de modo de exibição de cada vez. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

A maioria dos servidores de formulário implementar **SetViewContext** usando o algoritmo a seguir: 
  
- Cancelar o registro do formulário chamando o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) com **null** no parâmetro _pmnvs_ se já existir um contexto de modo de exibição para o formulário e depois ligue para [IUnknown:: Release do contexto modo de exibição](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) método a diminuir sua contagem de referência. 
    
- Se o novo contexto de modo de exibição não for **nula**, a chamada **IMAPIViewContext::SetAdviseSink** usando o parâmetro _pViewContext_ para configurar uma nova exibição aconselhe coletor de eventos. 
    
- Se o novo contexto de modo de exibição não for **nula**, chame o método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar quais sinalizadores de status foram definidos. 
    
- Se o novo contexto de modo de exibição não for **nula**, armazená-lo e chamar o método [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência. 
    
- Atualize quaisquer elementos de interface do usuário que dependem do contexto do modo de exibição. 
    
Dependendo os sinalizadores de status retornados de **IMAPIViewContext::GetViewStatus**, **SetViewContext** também pode realizar outras ações. Por exemplo, se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV forem retornados, **SetViewContext** pode habilitar os botões **próximo** e **anterior** para o novo contexto de modo de exibição. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa o método **IMAPIForm::SetViewContext** para definir o contexto de exibição do MFCMAPI no formulário antes que o formulário é exibido.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

