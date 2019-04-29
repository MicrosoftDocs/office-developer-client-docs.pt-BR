---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417403"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui uma subpasta.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da subpasta a ser excluída.
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido em _parâmetroulflags_.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla a exclusão da subpasta. Os seguintes sinalizadores podem ser definidos:
    
DEL_FOLDERS 
  
> Todas as subpastas da subpasta indicada por _lpEntryID_ devem ser excluídas. 
    
DEL_MESSAGES 
  
> Todas as mensagens na subpasta indicada por _lpEntryID_ devem ser excluídas. 
    
FOLDER_DIALOG 
  
> Um indicador de progresso deve ser exibido enquanto a operação prossegue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta especificada foi excluída com êxito.
    
MAPI_E_HAS_FOLDERS 
  
> A subpasta que está sendo excluída contém subpastas e o sinalizador DEL_FOLDERS não foi definido. As subpastas não foram excluídas.
    
MAPI_E_HAS_MESSAGES 
  
> A subpasta que está sendo excluída contém mensagens e o sinalizador DEL_MESSAGES não foi definido. A subpasta não foi excluída.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas nem todas as entradas foram excluídas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::D eletefolder** exclui uma subpasta. Por padrão, o **DeleteFolder** funciona apenas em pastas vazias, mas você pode usá-lo com êxito em pastas não vazias Configurando dois sinalizadores: DEL_FOLDERS e DEL_MESSAGES. Somente pastas vazias ou pastas que definem os sinalizadores DEL_FOLDERS e DEL_MESSAGES na chamada **DeleteFolder** podem ser excluídas. O DEL_FOLDERS permite que todas as subpastas da pasta sejam removidas; DEL_MESSAGES habilita todas as mensagens da pasta a serem removidas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando a operação de exclusão envolver mais de uma pasta, execute a operação o mais completo possível para cada pasta. Às vezes, uma das pastas a serem excluídas não existe ou foi movida ou copiada em outro lugar. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do seu controle, como a falta de memória, ficando sem espaço em disco ou corrupção no repositório de mensagens.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|O **DeleteFolder** excluiu com êxito todas as mensagens e subpastas.  <br/> |S_OK  <br/> |
|O **DeleteFolder** não pôde excluir com êxito todas as mensagens e subpastas.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro, exceto MAPI_E_NOT_FOUND  <br/> |
   
Quando o **DeleteFolder** não puder ser concluído, não presuma que nenhum trabalho foi realizado. O **DeleteFolder** pode ter sido capaz de excluir uma ou mais das mensagens e subpastas antes de encontrar o erro. 
  
Se uma ou mais subpastas não puderem ser excluídas, **DeleteFolder** retornará MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, dependendo da implementação do provedor de repositório de mensagens. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFolder::D eletefolder** para excluir pastas.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

