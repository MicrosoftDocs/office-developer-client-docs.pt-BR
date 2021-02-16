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
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430900"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o contexto de exibição atual do formulário. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parâmetros

 _ppViewContext_
  
> [out] Um ponteiro para um ponteiro para o contexto de exibição do formulário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O contexto de exibição atual do formulário foi retornado com êxito. 
    
S_FALSE 
  
> Não há contexto de exibição para o formulário.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **GetViewContext** para obter um ponteiro para o contexto de exibição estabelecido em uma chamada anterior para [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Se nenhuma chamada anterior tiver sido feita para **SetViewContext**, **GetViewContext**  _definirá ppViewContext_ como NULL. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Copie o ponteiro de contexto de exibição do formulário para o ponteiro passado pelo visualizador do formulário de chamada no _parâmetro ppViewContext._ Se o formulário não tiver um contexto de exibição, de definida  _ppViewContext_ como NULL. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o **método IMAPIForm::GetViewContext** para verificar se um formulário tem um contexto de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

