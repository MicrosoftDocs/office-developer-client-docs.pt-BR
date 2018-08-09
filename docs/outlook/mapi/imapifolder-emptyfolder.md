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
ms.openlocfilehash: 7d8653b8f0cb2196319c4a9c2b4bca89c8be5a24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766991"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**Aplica-se a**: Outlook 
  
Exclui todas as mensagens e subpastas de uma pasta sem excluir na pasta propriamente dita.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a pasta será esvaziada. Sinalizadores a seguir podem ser definidos:
    
DEL_ASSOCIATED 
  
> Exclui todas as subpastas, incluindo subpastas que contêm mensagens com conteúdo associado. O sinalizador DEL_ASSOCIATED tem significado apenas para a pasta de nível superior que a chamada atua no.
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo aquelas excluída.
    
FOLDER_DIALOG 
  
> Exibe um indicador de progresso enquanto continua a operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A pasta foi esvaziada com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas a pasta não foi esvaziada completamente. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir na pasta propriamente dita. 
  
Durante uma chamada de **EmptyFolder** , as mensagens enviadas não são excluídas. 
  
Conteúdo de uma pasta associado incluem mensagens que são usadas para descrever o armazenamento de soluções personalizadas, regras, formulários personalizados e modos de exibição e também podem incluir as definições do formulário. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Não chame o método [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foram enviadas. Mensagens enviadas não são excluídas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**EmptyFolder** com êxito tem esvaziada a pasta.  <br/> |S_OK  <br/> |
|**EmptyFolder** não pôde completamente esvazie a pasta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** não pôde concluir.  <br/> |Qualquer valor de erro  <br/> |
   
Quando **EmptyFolder** é impossível concluir, não presuma que foi feito nenhum trabalho. **EmptyFolder** podem ter sido capazes de excluir uma parte do conteúdo da pasta antes da ocorrência de erro. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI usa o método **IMAPIFolder::EmptyFolder** para excluir o conteúdo da pasta especificada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)

