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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766994"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**Aplica-se a**: Outlook 
  
Retorna o contexto de modo de exibição atual para o formulário. 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Par�metros

 _ppViewContext_
  
> [out] Um ponteiro para um ponteiro para o contexto de exibição do formulário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Contexto de modo de exibição atual do formulário foi retornado com êxito. 
    
S_FALSE 
  
> Não há nenhum contexto de modo de exibição para o formulário.
    
## <a name="remarks"></a>Coment�rios

Visualizadores de formulário chame **GetViewContext** para obter um ponteiro para o contexto de modo de exibição estabelecido em uma chamada anterior para [IMAPIForm::SetViewContext](imapiform-setviewcontext.md). Se nenhuma chamada anterior foi feita para **SetViewContext**, **GetViewContext** define _ppViewContext_ como NULL. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Copie o ponteiro de contexto do modo de exibição do formulário para o ponteiro transmitido pelo Visualizador formulário chamada no parâmetro _ppViewContext_ . Se o formulário não terá um contexto de modo de exibição, defina _ppViewContext_ como NULL. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI usa o método **IMAPIForm::GetViewContext** para verificar se um formulário tem um contexto de modo de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

