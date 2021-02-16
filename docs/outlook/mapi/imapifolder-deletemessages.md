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
  
> [in] Um ponteiro para uma [estrutura ENTRYLIST](entrylist.md) que contém o número de mensagens a excluir e uma matriz de estruturas [ENTRYID](entryid.md) que identificam as mensagens. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. O _parâmetro ulUIParam é_ ignorado, a menos que o MESSAGE_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido no _parâmetro ulFlags._ 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como as mensagens são excluídas. Os sinalizadores a seguir podem ser definidos:
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo as excluídas de forma suave.
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso à medida que a operação prosse segue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem ou mensagens especificadas foram excluídas com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as mensagens foram excluídas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::D eleteMessages** exclui mensagens de uma pasta. Mensagens que não existem, que foram movidas para outro lugar, abertas com permissão de leitura/gravação ou que estão enviadas atualmente não podem ser excluídas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando a operação de exclusão envolver mais de uma mensagem, execute a operação o mais completamente possível para cada pasta, mesmo se uma ou mais das mensagens não puderem ser excluídas. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere esses valores de retorno sob as seguintes condições.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**DeleteMessages** excluiu todas as mensagens com êxito.  <br/> |S_OK  <br/> |
|**DeleteMessages** não pôde excluir todas as mensagens e subpastas com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** não pôde ser concluído.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando **DeleteMessages** não puder ser concluído, não suponha que nenhum trabalho foi feito. **DeleteMessages** pode ter sido capaz de excluir uma ou mais das mensagens antes de encontrar o erro. 
  
 **DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o **método IMAPIFolder::D eleteMessages** para excluir as mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

