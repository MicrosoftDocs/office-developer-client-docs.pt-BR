---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416780"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui todas as mensagens e subpastas de uma pasta sem excluir a própria pasta.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. O _parâmetro ulUIParam é_ ignorado, a menos que o FOLDER_DIALOG padrão seja definido no parâmetro _ulFlags._ 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O _parâmetro lpProgress_ é ignorado, a menos que o FOLDER_DIALOG padrão seja definido no _parâmetro ulFlags._ 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a pasta é esvaziada. Os sinalizadores a seguir podem ser definidos:
    
DEL_ASSOCIATED 
  
> Exclui todas as subpastas, incluindo subpastas que contêm mensagens com conteúdo associado. O DEL_ASSOCIATED sinalizador tem significado apenas para a pasta de nível superior em que a chamada atua.
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo as excluídas de forma suave.
    
FOLDER_DIALOG 
  
> Exibe um indicador de progresso enquanto a operação prosse segue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta foi esvaziada com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas a pasta não foi completamente esvaziada. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir a própria pasta. 
  
Durante uma **chamada EmptyFolder,** as mensagens enviadas não são excluídas. 
  
O conteúdo associado de uma pasta inclui mensagens que são usadas para descrever exibições, regras, formulários personalizados e armazenamento de soluções personalizado, e também podem incluir definições de formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não chame o [método IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foram enviadas. As mensagens enviadas não são excluídas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere esses valores de retorno sob as seguintes condições.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**EmptyFolder** esvaziou a pasta com êxito.  <br/> |S_OK  <br/> |
|**EmptyFolder** não pôde esvaziar completamente a pasta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Quando **EmptyFolder** não puder ser concluída, não suponha que nenhum trabalho foi feito. **EmptyFolder** pode ter sido capaz de excluir parte do conteúdo da pasta antes de encontrar o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI usa o **método IMAPIFolder::EmptyFolder** para excluir o conteúdo da pasta especificada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

