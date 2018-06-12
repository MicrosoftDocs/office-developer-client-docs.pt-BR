---
title: IMessageDeleteAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767389"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Aplica-se a**: Outlook 
  
Exclui um anexo.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulAttachmentNum_
  
> [in] Número de índice do anexo para excluir. Esse é o valor da propriedade de **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.
    
 _ulUIParam_
  
> [in] Identificador da janela pai de todas as caixas de diálogo ou windows que esse método exibe. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador ATTACH_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador ATTACH_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores que controla a exibição de uma interface do usuário. O seguinte sinalizador pode ser definido:
    
ATTACH_DIALOG 
  
> Solicita a exibição de um indicador de progresso conforme continua a operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O anexo foi excluído com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IMessage::DeleteAttach** exclui um anexo de dentro de uma mensagem. 
  
Um anexo excluído não é permanentemente excluído até que o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem foi chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Antes de chamar **DeleteAttach**, chame o método de **IUnknown:: Release** para o anexo e cada um dos seus fluxos. 
  
Como a exclusão de um anexo pode ser um processo demorado, **DeleteAttach** fornece o mecanismo que exibe um indicador de progresso. Você pode solicitar a exibição de um indicador de progresso ao passar um ponteiro para sua [IMAPIProgress: IUnknown](imapiprogressiunknown.md) implementação ou NULL se você não tiver uma implementação. Você também deve especificar um identificador de janela no parâmetro _ulUIParam_ e o sinalizador ATTACH_DIALOG no parâmetro _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMessage::DeleteAttach** para excluir o anexo selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

