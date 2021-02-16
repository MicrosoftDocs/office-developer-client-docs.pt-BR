---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321361"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Move a mensagem atual para uma pasta.
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parâmetros

 _pFolderDestination_
  
> [in] Um ponteiro para a pasta para a qual a mensagem deve ser movida.
    
 _pViewContext_
  
> [in] Um ponteiro para um objeto de contexto de exibição.
    
 _prcPosRect_
  
> [in] Um ponteiro para uma [estrutura RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário atual. O próximo formulário exibido também usa esse retângulo de janela. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagens.
    
## <a name="remarks"></a>Comentários

Os objetos de formulário chamam o método **IMAPIMessageSite::MoveMessage** para mover a mensagem atual para uma nova pasta. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

A implementação de **MoveMessage** de um visualizador de formulário deve chamar o método [IMAPIViewContext::ActivateNext,](imapiviewcontext-activatenext.md) passando o sinalizador VCDIR_MOVE, antes de realmente mover a mensagem para uma nova pasta. Para obter a **estrutura RECT** usada pela janela de um formulário, chame a função [Windows GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Para uma lista de interfaces relacionadas a servidores de formulário, consulte [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Após o retorno de **MoveMessage**, os formulários devem verificar se há uma mensagem atual e, em seguida, descartar a si mesmos se não existe. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Não implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

