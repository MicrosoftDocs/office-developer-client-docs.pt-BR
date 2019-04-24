---
title: IMAPIFolderSetReadFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetReadFlags
api_type:
- COM
ms.assetid: 95a40c8a-0a8b-46c7-a07a-cbc6a7de8a3c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 15504ecc88188ed7bc4eed0e64b1871dbc6a5e8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350985"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais das mensagens da pasta e gerencia o envio de relatórios de leitura. 
  
```cpp
HRESULT SetReadFlags(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

_lpMsgList_
  
> no Um ponteiro para uma matriz de [](entrylist.md) estruturas ENTRYLIST que identificam a mensagem ou mensagens que têm sinalizadores de leitura para definir ou desmarcar. Se _lpMsgList_ estiver definido como NULL, os sinalizadores de leitura para todas as mensagens da pasta serão definidos ou apagados. 
    
_ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
_lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.
    
_ulFlags_
  
> no Uma bitmask de sinalizadores que controla a configuração do sinalizador de leitura de uma mensagem e o processamento de relatórios de leitura. Os seguintes sinalizadores podem ser definidos:
    
  - CLEAR_READ_FLAG: o sinalizador MSGFLAG_READ deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de leitura não deve ser enviado. 
        
  - CLEAR_NRN_PENDING: o sinalizador MSGFLAG_NRN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório não lido não deve ser enviado. 
        
  - CLEAR_RN_PENDING: o sinalizador MSGFLAG_RN_PENDING deve ser limpo no **PR_MESSAGE_FLAGS** e um relatório de leitura não deve ser enviado. 
        
  - GENERATE_RECEIPT_ONLY: um relatório de leitura deverá ser enviado se um estiver pendente, mas não houver nenhuma alteração no estado do sinalizador MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: permite que o **SetReadFlags** seja retornado com êxito, possivelmente antes da conclusão da operação. 
        
  - MESSAGE_DIALOG: exibe um indicador de progresso enquanto a operação prossegue.
    
  - SUPPRESS_RECEIPT: um relatório de leitura pendente deve ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada alterar o estado da mensagem de não lidos para leitura. Se essa chamada não alterar o estado da mensagem, o provedor de repositório de mensagens poderá ignorar esse sinalizador.
    
## <a name="return-values"></a>Valor de retorno

S_OK 
  
> O sinalizador de leitura para a mensagem ou mensagens especificadas foi definido ou limpo com êxito.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de repositório de mensagens não oferece suporte à supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações incompatíveis de sinalizadores é definida no parâmetro _parâmetroulflags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as mensagens foram processadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais das mensagens da pasta. Definir o sinalizador MSGFLAG_READ marca uma mensagem como lida, o que não indica necessariamente que o destinatário pretendido realmente leu a mensagem. 
  
O **SetReadFlags** também gerencia o envio de relatórios de leitura. 
  
O sinalizador de leitura não pode ser alterado para o seguinte:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas em outro lugar.
    
- Mensagens abertas com permissão de leitura/gravação.
    
- Mensagens que estão sendo enviadas.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode decidir não oferecer suporte ao envio de relatórios de leitura e à solicitação para suprimir relatórios de leitura. Para evitar a supressão de um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** for chamado com SUPPRESS_RECEIPT definido no parâmetro _parâmetroulflags_ . 
  
Quando o parâmetro _lpMsgList_ aponta para mais de uma mensagem, execute a operação o mais completo possível para cada mensagem. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens. 
  
Se nenhum dos sinalizadores estiver definido no parâmetro _parâmetroulflags_ , as seguintes regras serão aplicadas: 
  
- Se MSGFLAG_READ já estiver definido, não faça nada.
    
- Se MSGFLAG_READ não estiver definido, defina-o imediatamente e envie quaisquer relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.
    
Quando o sinalizador SUPPRESS_RECEIPT é definido, as seguintes regras são aplicadas:
  
- Se MSGFLAG_READ já estiver definido, não faça nada. 
    
- Se MSGFLAG_READ não estiver definido, defina-o e cancele todos os relatórios de leitura pendentes.
    
Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de cada mensagem e não envie relatórios de leitura. 
  
Quando o sinalizador GENERATE_RECEIPT_ONLY estiver definido, envie quaisquer relatórios de leitura pendentes. Não defina ou desmarque MSGFLAG_READ.
  
Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estiverem definidos, defina **PR_READ_RECEIPT_REQUESTED** como false se ele estiver definido e não enviar um relatório de leitura. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor retornado**|
|:-----|:-----|
|**SetReadFlags** processou com êxito todas as mensagens.  <br/> |S_OK  <br/> |
|O **SetReadFlags** não pôde processar com êxito todas as mensagens.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** não pôde ser concluída.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando o **SetReadFlags** não puder ser concluído, não presuma que nenhum trabalho foi realizado. **SetReadFlags** pode ter sido capaz de definir ou desmarcar o sinalizador MSGFLAG_READ para uma ou mais das mensagens antes de encontrar o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnSetReadFlag  <br/> |MFCMAPI usa o método **IMAPIFolder:: SetReadFlags** para definir manualmente o status de leitura nas mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriedade canônica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)  
- [Usando macros para tratamento de erros](using-macros-for-error-handling.md)

