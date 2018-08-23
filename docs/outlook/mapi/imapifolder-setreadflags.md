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
ms.openlocfilehash: 88185efea344844016547d0844277de6e0d661db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578315"
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
  
> [in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens que leu sinalizadores para definir ou limpar. Se _lpMsgList_ for definido como NULL, leia sinalizadores para todas as mensagens da pasta são definidas ou desmarcadas. 
    
_ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ . 
    
_lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação do MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.
    
_ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a configuração de sinalizador de leitura da mensagem e o processamento de ler relatórios. Sinalizadores a seguir podem ser definidos:
    
  - CLEAR_READ_FLAG: O sinalizador MSGFLAG_READ deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de leitura. 
        
  - CLEAR_NRN_PENDING: O sinalizador MSGFLAG_NRN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório não lido. 
        
  - CLEAR_RN_PENDING: O sinalizador MSGFLAG_RN_PENDING deve ser limpo em **PR_MESSAGE_FLAGS** e não deve ser enviado a um relatório de leitura. 
        
  - GENERATE_RECEIPT_ONLY: Um relatório de leitura deverão ser enviado se um está pendente, mas não deve haver nenhuma alteração no estado do sinalizador MSGFLAG_READ.
        
  - MAPI_DEFERRED_ERRORS: Permite **SetReadFlags** retornar com êxito, possivelmente antes que a operação for concluída. 
        
  - MESSAGE_DIALOG: Exibe um indicador de progresso enquanto continua a operação.
    
  - SUPPRESS_RECEIPT: Um relatório de leitura pendente deve ser cancelado se um relatório de leitura tivesse sido solicitado e essa chamada altera o estado da mensagem de não lido para ler. Se essa chamada não alterar o estado da mensagem, o provedor de armazenamento de mensagem pode ignorar esse sinalizador.
    
## <a name="return-values"></a>Valores de retorno

S_OK 
  
> O sinalizador de leitura para a mensagem especificada ou mensagens com êxito foi definido ou estiver desmarcado.
    
MAPI_E_NO_SUPPRESS 
  
> O provedor de armazenamento de mensagem não suporta a supressão de relatórios de leitura.
    
MAPI_E_INVALID_PARAMETER 
  
> Uma das seguintes combinações incompatíveis dos sinalizadores está definida no parâmetro _ulFlags_ : 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG 
    
   - SUPPRESS_RECEIPT | CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
   - CLEAR_READ_FLAG | GENERATE_RECEIPT_ONLY
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as mensagens foram processadas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::SetReadFlags** define ou limpa o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** de uma ou mais das mensagens da pasta. Definindo o sinalizador MSGFLAG_READ marca uma mensagem como lida, que não necessariamente indica que o destinatário pretendido realmente leu a mensagem. 
  
**SetReadFlags** também gerencia o envio de relatórios de leitura. 
  
O sinalizador de leitura não pode ser alterado para o seguinte:
  
- Mensagens que não existem.
    
- Mensagens que foram movidas para outro lugar.
    
- Mensagens que estão abertas com permissão de leitura/gravação.
    
- Mensagens que atualmente são enviadas.
    
## <a name="notes-to-implementers"></a>Notas para implementadores

Você pode decidir não suportam o envio de relatórios de leitura e a solicitação para suprimir a leitura de relatórios. Para evitar suprimindo a um relatório de leitura, retorne MAPI_E_NO_SUPPRESS quando **SetReadFlags** é chamado com SUPPRESS_RECEIPT definido no parâmetro _ulFlags_ . 
  
Quando o parâmetro _lpMsgList_ aponta para mais de uma mensagem, execute a operação como completamente para cada mensagem. Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem. 
  
Se nenhum dos sinalizadores estão definidos no parâmetro _ulFlags_ , as seguintes regras se aplicam: 
  
- Se MSGFLAG_READ já estiver definida, nada a fazer.
    
- Se MSGFLAG_READ não estiver definida, defini-lo imediatamente e enviar pendentes de relatórios de leitura, se a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) é definida.
    
Quando o sinalizador SUPPRESS_RECEIPT é definido, as seguintes regras se aplicam:
  
- Se MSGFLAG_READ já estiver definida, nada a fazer. 
    
- Se MSGFLAG_READ não estiver definida, defini-la e Cancelar pendentes de relatórios de leitura.
    
Quando o sinalizador CLEAR_READ_FLAG estiver definido, desmarque o sinalizador MSGFLAG_READ na propriedade **PR_MESSAGE_FLAGS** do cada mensagem e não enviar todos os relatórios leitura. 
  
Quando o sinalizador GENERATE_RECEIPT_ONLY é definido, envie todos os relatórios leitura pendentes. Faça MSGFLAG_READ não definir ou limpar.
  
Quando os SUPPRESS_RECEIPT GENERATE_RECEIPT_ONLY sinalizadores e estiverem definidos, defina **PR_READ_RECEIPT_REQUESTED** como FALSE se ele estiver definido e não enviar um relatório de leitura. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**SetReadFlags** tem processadas com êxito a cada mensagem.  <br/> |S_OK  <br/> |
|**SetReadFlags** não pôde processar com êxito a cada mensagem.  <br/> |MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND  <br/> |
|**SetReadFlags** não pôde concluir.  <br/> |Qualquer valor de erro, exceto E_NOT_FOUND  <br/> |
   
Quando **SetReadFlags** é impossível concluir, não presuma que foi feito nenhum trabalho. **SetReadFlags** podem ter sido capaz de definir ou limpar o sinalizador MSGFLAG_READ para uma ou mais das mensagens antes da ocorrência de erro. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSetReadFlag  <br/> |MFCMAPI usa o método **IMAPIFolder::SetReadFlags** para definir manualmente o status de leitura em todas as mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [ENTRYLIST](entrylist.md) 
- [IMessage::SetReadFlag](imessage-setreadflag.md)  
- [Propriedade canônica PidTagMessageFlags](pidtagmessageflags-canonical-property.md)  
- [Propriedade canônica PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)  
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)  
- [Usar macros para lidar com erros](using-macros-for-error-handling.md)

