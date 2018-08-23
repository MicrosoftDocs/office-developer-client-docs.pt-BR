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
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578630"
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
  
> [in] Um ponteiro para uma estrutura [ENTRYLIST](entrylist.md) que contém o número de mensagens para excluir e uma matriz de estruturas [ENTRYID](entryid.md) que identificam as mensagens. 
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as mensagens são excluídas. Sinalizadores a seguir podem ser definidos:
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo aquelas excluída.
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso conforme continua a operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem especificada ou mensagens foram excluídas com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as mensagens foram excluídas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::DeleteMessages** exclui mensagens de uma pasta. Mensagens que não existem, que foram movidos em outro lugar, que estão abertos com permissão de leitura/gravação ou que são enviados atualmente não podem ser excluídas. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando a operação de exclusão envolve mais de uma mensagem, execute a operação como completamente para cada pasta, mesmo se um ou mais das mensagens não podem ser excluídas. Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**DeleteMessages** excluiu com êxito a cada mensagem.  <br/> |S_OK  <br/> |
|**DeleteMessages** não pôde ser excluído com êxito a cada mensagem e a subpasta.  <br/> |MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND  <br/> |
|**DeleteMessages** não pôde concluir.  <br/> |Qualquer valor de erro, exceto E_NOT_FOUND  <br/> |
   
Quando **DeleteMessages** é impossível concluir, não presuma que foi feito nenhum trabalho. **DeleteMessages** podem ter sido capaz de excluir uma ou mais das mensagens antes da ocorrência de erro. 
  
 **DeleteMessages** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do armazenamento de mensagens. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFolder::DeleteMessages** para excluir as mensagens especificadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)

