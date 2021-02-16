---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335757"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um token numérico que o [método IMAPISession::ShowForm](imapisession-showform.md) usa para acessar uma mensagem. 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a mensagem. Passar **resultados** nulos na interface padrão ou [IMessage](imessageimapiprop.md), sendo usado. O  _parâmetro lpInterface_ deve ser **nulo** ou IID_IMessage. 
    
 _lpMessage_
  
> [in] Um ponteiro para a mensagem a ser exibida no formulário.
    
 _lpulMessageToken_
  
> [out] Um ponteiro para um token de mensagem, que é usado pelo método **IMAPISession::ShowForm** para acessar a mensagem apontada por  _lpMessage_.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A preparação do formulário foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::P repareForm** cria um token de mensagem para a mensagem apontada pelo parâmetro  _lpMessage_ e chama o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) da mensagem. Esse token é passado no  _parâmetro ulMessageToken_ para **IMAPISession::ShowForm**. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se a chamada para **PrepareForm** for bem-sucedida, libere a mensagem apontada por  _lpMessage_ chamando seu método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) antes de chamar **ShowForm**. A falha ao liberar a mensagem antes de chamar **ShowForm** pode causar vazamentos de memória. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI usa o **método IMAPISession::P repareForm,** juntamente com **IMAPISession::ShowForm**, para exibir uma mensagem em um formulário modal.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

