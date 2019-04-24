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
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350943"
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
  
> no Um ponteiro para o novo contexto de exibição do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O contexto de exibição foi definido com êxito.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIForm:: SetViewContext** para estabelecer um determinado contexto de modo de exibição de formulário como atual. Um formulário pode ter apenas um contexto de exibição por vez. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A maioria dos servidores de formulários implementa o **SetViewContext** usando o seguinte algoritmo: 
  
- Se já existir um contexto de modo de exibição para o formulário, cancele o registro do formulário chamando o método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) com **nulo** no parâmetro _pmnvs_ e, em seguida, chame o formato de contexto de exibição [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) método para decrementar sua contagem de referência. 
    
- Se o novo contexto de exibição não for **nulo**, chame **IMAPIViewContext:: SetAdviseSink** usando o parâmetro _pViewContext_ para configurar um novo coletor de aviso de modo de exibição. 
    
- Se o novo contexto de exibição não for **nulo**, chame o método [IMAPIViewContext:: GetViewStatus](imapiviewcontext-getviewstatus.md) para determinar quais sinalizadores de status foram definidos. 
    
- Se o novo contexto de exibição não for **nulo**, armazene-o e chame seu método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência. 
    
- Atualize todos os elementos da interface do usuário que dependem do contexto de exibição. 
    
Dependendo dos sinalizadores de status retornados de **IMAPIViewContext:: GetViewStatus**, **SetViewContext** também pode executar outras ações. Por exemplo, se os sinalizadores VCSTATUS_NEXT e VCSTATUS_PREV forem retornados, **SetViewContext** poderá habilitar os botões **próximo** e **anterior** para o novo contexto de modo de exibição. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI usa o método **IMAPIForm:: SetViewContext** para definir o contexto de exibição de MFCMAPI no formulário antes de o formulário ser exibido.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

