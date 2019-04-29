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
  
> no Ponteiro para um objeto de coletor de aviso de formulário ou nulo.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O registro ou cancelamento da notificação de formulário foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

Os objetos Form chamam o método **IMAPIViewContext:: SetAdviseSink** para registrar para saber mais sobre as alterações no Visualizador de formulários ou cancelar um registro anterior. Quando _pmvns_ é definido como nulo, o formulário deseja cancelar um registro. Quando o _pmvns_ aponta para um coletor de aviso de formulário válido, o formulário deseja se registrar para notificações futuras. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando o **SetAdviseSink** inclui um ponteiro de coletor de aviso de formulário, mantenha uma referência a ele até que outra chamada de **SetAdviseSink** seja feita para cancelar a notificação. Enviar uma notificação quando uma alteração ocorrer no seu visualizador e quando você estiver carregando uma nova mensagem. 
  
Para obter mais informações, consulte [envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: SetAdviseSink  <br/> |MFCMAPI implementa o método **IMAPIViewContext:: SetAdviseSink** nesta função.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

