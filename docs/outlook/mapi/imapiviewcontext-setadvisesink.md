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
ms.openlocfilehash: abee768dd29cc807b605a7d13570a579cb271b2c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767365"
---
# <a name="imapiviewcontextsetadvisesink"></a>IMAPIViewContext::SetAdviseSink

  
  
**Aplica-se a**: Outlook 
  
Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador. 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a>Parâmetros

 _pmvns_
  
> [in] Ponteiro para um formulário avise o objeto coletor de eventos ou nulo.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O registro ou cancelamento de notificação de formulário foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método de **IMAPIViewContext::SetAdviseSink** para registrar-se para aprender sobre alterações no Visualizador do formulário ou cancelar um registro prévio. Quando _pmvns_ estiver definido como nulo, o formulário deseja cancelar um registro. Quando o coletor de eventos de aviso de pontos de _pmvns_ para um formulário válido, o formulário quer registrar para notificações futuras. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando o **SetAdviseSink** inclui um formulário ponteiro coletor de eventos de aviso, mantenha uma referência a ele até que a outra chamada **SetAdviseSink** é feita de cancelar a notificação. Envie uma notificação quando ocorre uma alteração no seu visualizador e ao carregar uma nova mensagem. 
  
Para obter mais informações, consulte [enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::SetAdviseSink  <br/> |MFCMAPI implementa o método **IMAPIViewContext::SetAdviseSink** nessa função.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

