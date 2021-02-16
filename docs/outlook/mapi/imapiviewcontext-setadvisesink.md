---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419391"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parâmetros

 _pmvns_
  
> [in] Ponteiro para um objeto sink de aconselhmento de formulário ou NULL.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro ou cancelamento para notificação de formulário foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chamam o método **IMAPIViewContext::SetAdviseSink** para se registrar para saber mais sobre alterações no visualizador de formulário ou cancelar um registro anterior. Quando  _pmvns_ é definido como NULL, o formulário deseja cancelar um registro. Quando  _pmvns aponta_ para um sink de aviso de formulário válido, o formulário deseja se registrar para notificações futuras. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando **SetAdviseSink** inclui um ponteiro de pia de aviso de formulário, mantenha uma referência a ele até que outra chamada **SetAdviseSink** seja feita para cancelar a notificação. Envie uma notificação quando ocorrer uma alteração no visualizador e quando você estiver carregando uma nova mensagem. 
  
Para obter mais informações, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementa o **método IMAPIViewContext::SetAdviseSink** nesta função.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

