---
title: IMessageSetReadFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.SetReadFlag
api_type:
- COM
ms.assetid: 2d02ebf6-bb8b-42bb-9bd0-870dbae9aeb4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 874dba4aa18190792a52e29064155f5afa0ef44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439867"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem e gerencia o envio de relatórios de leitura.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_ulFlags_
  
> no Bitmask de sinalizadores que controlam a configuração do sinalizador de leitura de uma mensagem ou seja, o sinalizador MSGFLAG_READ da mensagem em sua propriedade **PR_MESSAGE_FLAGS** e o processamento de relatórios de leitura. Os seguintes sinalizadores podem ser definidos: 
    
  - CLEAR_READ_FLAG: o sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório de leitura deve ser enviado. 
      
  - CLEAR_NRN_PENDING: o sinalizador MSGFLAG_NRN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de não leitura não deve ser enviado. 
      
  - CLEAR_RN_PENDING: o sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório de leitura deve ser enviado. 
      
  - GENERATE_RECEIPT_ONLY: um relatório de leitura deverá ser enviado se um estiver pendente, mas não houver nenhuma alteração no estado do sinalizador MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: permite que o **SetReadFlag** seja retornado com êxito, possivelmente antes da conclusão da operação. 
      
  - SUPPRESS_RECEIPT: um relatório de leitura pendente deve ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada alterar o estado da mensagem de não lidos para leitura. Se essa chamada não alterar o estado da mensagem, o provedor de repositório de mensagens poderá ignorar esse sinalizador.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O sinalizador de leitura da mensagem foi definido ou limpo com êxito.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de repositório de mensagens não oferece suporte à supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações de sinalizadores é definida no parâmetro _parâmetroulflags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Comentários

O método **IMessage:: SetReadFlag** define ou limpa o sinalizador MSGFLAG_READ da mensagem na propriedade **PR_MESSAGE_FLAGS** e chama [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para salvar a mensagem. Definir o sinalizador MSGFLAG_READ marca uma mensagem como tendo sido lida, o que não necessariamente indica que o destinatário pretendido realmente leu a mensagem. 
  
O **SetReadFlags** também gerencia o envio de relatórios de leitura. Um relatório de leitura é enviado somente se o remetente solicitou um. 
  
O sinalizador de leitura não pode ser alterado para:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas em outro lugar.
    
- Mensagens abertas com permissão de leitura/gravação.
    
- Mensagens que estão sendo enviadas.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Se nenhum dos sinalizadores estiver definido no parâmetro _parâmetroulflags_ , as seguintes regras serão aplicadas: 
  
- Se MSGFLAG_READ já estiver definido, não faça nada.
    
- Se MSGFLAG_READ não estiver definido, defina-o e envie quaisquer relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.
    
Se os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, o bit PR_READ_RECEIPT_REQUESTED, se definido, deverá ser limpo e um relatório de leitura não deverá ser enviado.
  
Quando o sinalizador SUPPRESS_RECEIPT estiver definido:
  
- Se MSGFLAG_READ já estiver definido, não faça nada. 
    
- Se MSGFLAG_READ não estiver definido, defina-o e cancele todos os relatórios de leitura pendentes.
    
Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de cada mensagem e não envie relatórios de leitura. 
  
Quando o sinalizador GENERATE_RECEIPT_ONLY estiver definido, envie quaisquer relatórios de leitura pendentes. Não defina ou desmarque MSGFLAG_READ.
  
Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, defina a propriedade PR_READ_RECEIPT_REQUESTED como FALSE se ela estiver definida e não enviar um relatório de leitura.
  
Você pode otimizar o comportamento do relatório eliminando a geração de relatórios de leitura sob determinadas condições. No enTanto, se você não oferecer suporte à supressão de relatórios e um cliente chama **SetReadFlag** com o sinalizador SUPPRESS_RECEIPT definido, retorne MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI usa o método **IMessage:: SetReadFlag** para definir sinalizadores de leitura em mensagens selecionadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage : IMAPIProp](imessageimapiprop.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

