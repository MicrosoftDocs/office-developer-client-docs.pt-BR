---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426069"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui uma ou mais mensagens.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMsgList_
  
> no Um ponteiro para uma [](entrylist.md) estrutura ENTRYLIST que contém o número de mensagens a serem excluídas e uma matriz de estruturas [EntryID](entryid.md) que identificam as mensagens. 
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam como as mensagens são excluídas. Os seguintes sinalizadores podem ser definidos:
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo as excluídas de forma reversível.
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso à medida que a operação prossegue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem ou mensagens especificadas foram excluídas com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as mensagens foram excluídas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::D eletemessages** exclui mensagens de uma pasta. As mensagens que não existem, que foram movidas em outro lugar, que estão abertas com permissão de leitura/gravação ou não podem ser excluídas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando a operação de exclusão envolve mais de uma mensagem, execute a operação o mais completo possível para cada pasta, mesmo que uma ou mais das mensagens não possam ser excluídas. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|O **DeleteMessages** excluiu com êxito todas as mensagens.  <br/> |S_OK  <br/> |
|O **DeleteMessages** não pôde excluir com êxito todas as mensagens e subpastas.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** não pôde ser concluída.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando o **DeleteMessages** não puder ser concluído, não presuma que nenhum trabalho foi realizado. O **DeleteMessages** pode ter sido capaz de excluir uma ou mais mensagens antes de encontrar o erro. 
  
 **DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do repositório de mensagens. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg. cpp  <br/> |CFolderDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFolder::D eletemessages** para excluir as mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

