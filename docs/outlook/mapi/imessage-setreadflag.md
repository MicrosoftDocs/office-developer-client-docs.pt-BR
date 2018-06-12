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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0ae35166f01f597c2c3ab399a1b66e5760ab0dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767388"
---
# <a name="imessagesetreadflag"></a>IMessage::SetReadFlag

**Aplica-se a**: Outlook 
  
Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem e gerencia o envio de relatórios de leitura.
  
```cpp
HRESULT SetReadFlag(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

_ulFlags_
  
> [in] Bitmask dos sinalizadores que controla a definição da leitura da mensagem ou seja, sinalizador sinalizador MSGFLAG_READ da mensagem em sua propriedade **PR_MESSAGE_FLAGS** e o processamento de relatórios de leitura. Sinalizadores a seguir podem ser definidos: 
    
  - CLEAR_READ_FLAG: O sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório leitura deve ser enviado. 
      
  - CLEAR_NRN_PENDING: O sinalizador MSGFLAG_NRN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de não-leitura. 
      
  - CLEAR_RN_PENDING: O sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e nenhum relatório leitura deve ser enviado. 
      
  - GENERATE_RECEIPT_ONLY: Um relatório de leitura deverão ser enviado se um está pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ.
      
  - MAPI_DEFERRED_ERRORS: Permite **SetReadFlag** retornar com êxito, possivelmente antes que a operação for concluída. 
      
  - SUPPRESS_RECEIPT: Um relatório de leitura pendente deve ser cancelado se um relatório de leitura tivesse sido solicitado e essa chamada altera o estado da mensagem de não lido para ler. Se essa chamada não alterar o estado da mensagem, o provedor de armazenamento de mensagem pode ignorar esse sinalizador.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Sinalizador de leitura da mensagem foi definida com êxito ou desmarcada.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de armazenamento de mensagem não suporta a supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações de sinalizadores está definida no parâmetro _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
## <a name="remarks"></a>Coment�rios

O método **IMessage::SetReadFlag** define ou limpa o sinalizador MSGFLAG_READ da mensagem na propriedade **PR_MESSAGE_FLAGS** e chamadas [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem. Definindo o sinalizador MSGFLAG_READ marca uma mensagem como tendo sido lida, que não necessariamente indica que o destinatário pretendido realmente leu a mensagem. 
  
**SetReadFlags** também gerencia o envio de relatórios de leitura. Um relatório de leitura é enviado somente se o remetente solicitou uma. 
  
O sinalizador de leitura não pode ser alterado para:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas para outro lugar.
    
- Mensagens que estão abertas com permissão de leitura/gravação.
    
- Mensagens que atualmente são enviadas.
    
## <a name="notes-to-callers"></a>Notas para chamadores

Se nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ , as seguintes regras se aplicam: 
  
- Se MSGFLAG_READ já estiver definida, nada a fazer.
    
- Se MSGFLAG_READ não estiver definida, defini-la e enviar pendentes de relatórios de leitura, se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) é definida.
    
Se os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, o PR_READ_RECEIPT_REQUESTED bit, se definido, deve ser limpo e não deve ser enviado a um relatório de leitura.
  
Quando o sinalizador SUPPRESS_RECEIPT é definido:
  
- Se MSGFLAG_READ já estiver definida, nada a fazer. 
    
- Se MSGFLAG_READ não estiver definida, defini-la e Cancelar pendentes de relatórios de leitura.
    
Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** do cada mensagem e não enviar todos os relatórios leitura. 
  
Quando o sinalizador GENERATE_RECEIPT_ONLY é definido, envie todos os relatórios leitura pendentes. Faça MSGFLAG_READ não definir ou limpar.
  
Quando os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, defina a propriedade PR_READ_RECEIPT_REQUESTED como FALSE se estiver definida e não enviar um relatório de leitura.
  
Você pode otimizar o comportamento de relatório por suprimindo a geração de relatórios de leitura sob certas condições. No entanto, se você não oferecem suporte a supressão de relatórios e um cliente chama **SetReadFlag** com o sinalizador SUPPRESS_RECEIPT definido, retorne MAPI_E_NO_SUPPRESS. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa o método **IMessage::SetReadFlag** para definir sinalizadores de leitura em mensagens selecionadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)  
- [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)  
- [IMAPIProp::GetProps](imapiprop-getprops.md)  
- [IMAPIProp::SaveChanges](imapiprop-savechanges.md) 
- [Propriedade canônico de PidTagMessageFlags](pidtagmessageflags-canonical-property.md) 
- [IMessage: IMAPIProp](imessageimapiprop.md)
- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

