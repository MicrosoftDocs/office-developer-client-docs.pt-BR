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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351076"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um anexo.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulAttachmentNum_
  
> no Número de índice do anexo a ser excluído. Este é o valor da propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.
    
 _ulUIParam_
  
> no Manipulador para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador ATTACH_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador ATTACH_DIALOG esteja definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Bitmask de sinalizadores que controla a exibição de uma interface de usuário. O seguinte sinalizador pode ser definido:
    
ATTACH_DIALOG 
  
> Solicita a exibição de um indicador de progresso à medida que a operação prossegue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi excluído com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMessage::D eleteattach** exclui um anexo de dentro de uma mensagem. 
  
Um anexo excluído não é excluído permanentemente até que o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem seja chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Antes de chamar **DeleteAttach**, chame o método **IUnknown:: Release** para o anexo e cada um de seus fluxos. 
  
Como a exclusão de um anexo pode ser um processo demorado, o **DeleteAttach** fornece o mecanismo que exibe um indicador de progresso. Você pode solicitar a exibição de um indicador de progresso passando um ponteiro para sua implementação [método imapiprogress: IUnknown](imapiprogressiunknown.md) ou nulo se não tiver uma implementação. Você também deve especificar um identificador de janela no parâmetro _ulUIParam_ e o sinalizador ATTACH_DIALOG no parâmetro _parâmetroulflags_ . 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AttachmentsDlg. cpp  <br/> |CAttachmentsDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMessage::D eleteattach** para excluir o anexo selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

