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
ms.openlocfilehash: e12ce442540930d9fa366ced073afc4828a01244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576110"
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
  
> [in] Um ponteiro para a pasta onde a mensagem deve ser movido.
    
 _pViewContext_
  
> [in] Um ponteiro para um objeto de contexto do modo de exibição.
    
 _prcPosRect_
  
> [in] Um ponteiro para uma estrutura de [Retangular](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contém o tamanho da janela e a posição atual do formulário. A próxima forma exibida também usa esse retângulo de janela. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_SUPPORT 
  
> A operação não é suportada por este site de mensagem.
    
## <a name="remarks"></a>Comentários

Objetos de formulário chame o método **IMAPIMessageSite::MoveMessage** para mover a mensagem atual para uma nova pasta. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

A implementação do Visualizador de um formulário de **MoveMessage** deve chamar o método [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) , passando o sinalizador VCDIR_MOVE, antes de realmente mover a mensagem para uma nova pasta. Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função do Windows [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Para obter uma lista das interfaces relacionadas aos servidores de formulário, consulte [Interfaces de formulário de MAPI](mapi-form-interfaces.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Após o retorno de **MoveMessage**, formulários devem verificar se há uma mensagem atual e, em seguida, descartar sozinhos, se não houver nenhum. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |Não foi implementado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Interfaces de formulário MAPI](mapi-form-interfaces.md)

