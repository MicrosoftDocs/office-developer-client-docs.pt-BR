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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430704"
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
  
> [in] Número de índice do anexo a ser excluído. Esse é o valor da propriedade PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) do anexo.
    
 _ulUIParam_
  
> [in] Alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam é_ ignorado, a menos que o ATTACH_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
 _lpProgress_
  
> [in] Ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador ATTACH_DIALOG seja definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores que controla a exibição de uma interface do usuário. O sinalizador a seguir pode ser definido:
    
ATTACH_DIALOG 
  
> Solicita a exibição de um indicador de progresso à medida que a operação prossesse.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O anexo foi excluído com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMessage::D eleteAttach** exclui um anexo de dentro de uma mensagem. 
  
Um anexo excluído não é excluído permanentemente até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem tenha sido chamado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Antes de **chamar DeleteAttach,** chame o **método IUnknown::Release** para o anexo e cada um de seus fluxos. 
  
Como a exclusão de um anexo pode ser um processo demorado, **DeleteAttach** fornece o mecanismo que exibe um indicador de progresso. Você pode solicitar a exibição de um indicador de progresso passando um ponteiro para seu [IMAPIProgress : implementação IUnknown](imapiprogressiunknown.md) ou NULL se você não tiver uma implementação. Você também deve especificar um alça de janela no _parâmetro ulUIParam_ e o sinalizador ATTACH_DIALOG no _parâmetro ulFlags._ 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o **método IMessage::D eleteAttach** para excluir o anexo selecionado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

