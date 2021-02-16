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
  
> [in] Máscara de bits de sinalizadores que controla a configuração do sinalizador de leitura de uma mensagem, ou seja, o sinalizador de MSGFLAG_READ da mensagem em sua propriedade **PR_MESSAGE_FLAGS** e o processamento de relatórios de leitura. Os sinalizadores a seguir podem ser definidos: 
    
  - CLEAR_READ_FLAG: o MSGFLAG_READ sinalizador deve ser limpo **PR_MESSAGE_FLAGS** relatório de leitura deve ser enviado. 
      
  - CLEAR_NRN_PENDING: o MSGFLAG_NRN_PENDING sinalizador deve ser limpo **no** PR_MESSAGE_FLAGS e um relatório de não leitura não deve ser enviado. 
      
  - CLEAR_RN_PENDING: o MSGFLAG_RN_PENDING sinalizador deve ser limpo **PR_MESSAGE_FLAGS** relatório de leitura deve ser enviado. 
      
  - GENERATE_RECEIPT_ONLY: um relatório de leitura deve ser enviado se houver um pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ leitura.
      
  - MAPI_DEFERRED_ERRORS: permite que **SetReadFlag** retorne com êxito, possivelmente antes da conclusão da operação. 
      
  - SUPPRESS_RECEIPT: um relatório de leitura pendente deverá ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada mudar o estado da mensagem de não lida para lida. Se essa chamada não alterar o estado da mensagem, o provedor do armazenamento de mensagens poderá ignorar esse sinalizador.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O sinalizador de leitura da mensagem foi definido ou limpo com êxito.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de armazenamento de mensagens não suporta a supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações de sinalizadores é definida no _parâmetro ulFlags:_ 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Comentários

O método **IMessage::SetReadFlag** define ou limpa o sinalizador MSGFLAG_READ da mensagem na propriedade PR_MESSAGE_FLAGS e chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar **a** mensagem. A definição MSGFLAG_READ sinalizador marca uma mensagem como tendo sido lida, o que não indica necessariamente que o destinatário pretendido realmente leu a mensagem. 
  
**SetReadFlags** também gerencia o envio de relatórios de leitura. Um relatório de leitura é enviado somente se o remetente solicitou um. 
  
O sinalizador de leitura não pode ser alterado para:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas para outro lugar.
    
- Mensagens abertas com permissão de leitura/gravação.
    
- Mensagens enviadas no momento.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Se nenhum dos sinalizadores for definido no  _parâmetro ulFlags,_ as seguintes regras serão aplicadas: 
  
- Se MSGFLAG_READ já estiver definido, não faça nada.
    
- Se MSGFLAG_READ não estiver definida, de definida e envie relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.
    
Se os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estão definidos, o bit PR_READ_RECEIPT_REQUESTED, se definido, deve ser limpo e um relatório de leitura não deve ser enviado.
  
Quando o SUPPRESS_RECEIPT sinalizador está definido:
  
- Se MSGFLAG_READ já estiver definido, não faça nada. 
    
- Se MSGFLAG_READ não estiver definido, de definida-a e cancele quaisquer relatórios de leitura pendentes.
    
Quando o CLEAR_READ_FLAG sinalizador estiver definido, limpe o sinalizador MSGFLAG_READ na  propriedade PR_MESSAGE_FLAGS de cada mensagem e não envie nenhum relatório de leitura. 
  
Quando o GENERATE_RECEIPT_ONLY sinalizador estiver definido, envie relatórios de leitura pendentes. Não de definir ou limpar MSGFLAG_READ.
  
Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estão definidos, de definida a propriedade PR_READ_RECEIPT_REQUESTED como FALSE se estiver definida e não enviar um relatório de leitura.
  
Você pode otimizar o comportamento do relatório suprimindo a geração de relatórios de leitura sob determinadas condições. No entanto, se você não suportar a supressão de relatórios e um cliente chamar **SetReadFlag** com o sinalizador SUPPRESS_RECEIPT definido, retorne MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa o **método IMessage::SetReadFlag** para definir sinalizadores de leitura em mensagens selecionadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage : IMAPIProp](imessageimapiprop.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

