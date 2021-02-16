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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406910"
---
# <a name="imapifoldersetreadflags"></a>IMAPIFolder::SetReadFlags

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma ou mais mensagens da pasta e gerencia o envio de relatórios de leitura. 
  
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
  
> [in] Um ponteiro para uma matriz de [estruturas ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens que têm sinalizadores de leitura a definir ou limpar. Se  _lpMsgList_ for definido como NULL, os sinalizadores de leitura de todas as mensagens da pasta serão definidos ou limpos. 
    
_ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. O _parâmetro ulUIParam é_ ignorado, a menos que o MESSAGE_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
_lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido em  _ulFlags_.
    
_ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a configuração do sinalizador de leitura de uma mensagem e o processamento de relatórios de leitura. Os sinalizadores a seguir podem ser definidos:
    
  - CLEAR_READ_FLAG: o MSGFLAG_READ sinalizador deve ser limpo **PR_MESSAGE_FLAGS** um relatório de leitura não deve ser enviado. 
        
  - CLEAR_NRN_PENDING: o MSGFLAG_NRN_PENDING deve ser limpo **PR_MESSAGE_FLAGS** relatório não lido não deve ser enviado. 
        
  - CLEAR_RN_PENDING: o MSGFLAG_RN_PENDING sinalizador deve ser limpo **PR_MESSAGE_FLAGS** um relatório de leitura não deve ser enviado. 
        
  - GENERATE_RECEIPT_ONLY: um relatório de leitura deve ser enviado se houver um pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ leitura.
        
  - MAPI_DEFERRED_ERRORS: permite que **SetReadFlags** retorne com êxito, possivelmente antes da conclusão da operação. 
        
  - MESSAGE_DIALOG: exibe um indicador de progresso enquanto a operação continua.
    
  - SUPPRESS_RECEIPT: um relatório de leitura pendente deverá ser cancelado se um relatório de leitura tiver sido solicitado e essa chamada mudar o estado da mensagem de não lida para lida. Se essa chamada não alterar o estado da mensagem, o provedor do armazenamento de mensagens poderá ignorar esse sinalizador.
    
## <a name="return-values"></a>Valor de retorno

S_OK 
  
> O sinalizador de leitura da mensagem ou mensagens especificada foi definido ou limpo com êxito.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de armazenamento de mensagens não suporta a supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações incompatíveis de sinalizadores é definida no _parâmetro ulFlags:_ 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as mensagens foram processadas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais mensagens da pasta. Definir o MSGFLAG_READ marca uma mensagem como lida, o que não indica necessariamente que o destinatário pretendido realmente leu a mensagem. 
  
**SetReadFlags** também gerencia o envio de relatórios de leitura. 
  
O sinalizador de leitura não pode ser alterado para o seguinte:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas para outro lugar.
    
- Mensagens abertas com permissão de leitura/gravação.
    
- Mensagens enviadas no momento.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode decidir não suportar o envio de relatórios de leitura e a solicitação para suprimir relatórios de leitura. Para evitar suprimir um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** for chamado com SUPPRESS_RECEIPT definido no _parâmetro ulFlags._ 
  
Quando o  _parâmetro lpMsgList_ aponta para mais de uma mensagem, execute a operação o mais completamente possível para cada mensagem. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens. 
  
Se nenhum dos sinalizadores for definido no  _parâmetro ulFlags,_ as seguintes regras serão aplicadas: 
  
- Se MSGFLAG_READ já estiver definido, não faça nada.
    
- Se MSGFLAG_READ não estiver definida, de definida imediatamente e envie relatórios de leitura pendentes se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) estiver definida.
    
Quando o SUPPRESS_RECEIPT sinalizador estiver definido, as seguintes regras serão aplicadas:
  
- Se MSGFLAG_READ já estiver definido, não faça nada. 
    
- Se MSGFLAG_READ não estiver definido, de definida-a e cancele quaisquer relatórios de leitura pendentes.
    
Quando o CLEAR_READ_FLAG sinalizador estiver definido, limpe o sinalizador MSGFLAG_READ na  propriedade PR_MESSAGE_FLAGS de cada mensagem e não envie nenhum relatório de leitura. 
  
Quando o GENERATE_RECEIPT_ONLY sinalizador estiver definido, envie relatórios de leitura pendentes. Não de definir ou limpar MSGFLAG_READ.
  
Quando os sinalizadores SUPPRESS_RECEIPT e GENERATE_RECEIPT_ONLY estão definidos,  de definida PR_READ_RECEIPT_REQUESTED como FALSE se estiver definida e não enviar um relatório de leitura. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere esses valores de retorno sob as seguintes condições.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**SetReadFlags** processou todas as mensagens com êxito.  <br/> |S_OK  <br/> |
|**SetReadFlags** não pôde processar todas as mensagens com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**SetReadFlags** não pôde ser concluído.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando **SetReadFlags** não puder ser concluído, não suponha que nenhum trabalho foi feito. **SetReadFlags** pode ter sido capaz de definir ou limpar o sinalizador de MSGFLAG_READ para uma ou mais mensagens antes de encontrar o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa o **método IMAPIFolder::SetReadFlags** para definir manualmente o status de leitura nas mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriedade canônica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)  
- [Usando macros para tratamento de erros](using-macros-for-error-handling.md)

