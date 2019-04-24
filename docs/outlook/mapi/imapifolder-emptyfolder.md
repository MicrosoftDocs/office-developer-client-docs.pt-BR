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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280103"
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
  
> no Uma alça para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpProgress_
  
> no Um ponteiro para um objeto Progress que exibe um indicador de progresso. Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a pasta é esvaziada. Os seguintes sinalizadores podem ser definidos:
    
DEL_ASSOCIATED 
  
> Exclui todas as subpastas, incluindo as subpastas que contêm mensagens com conteúdo associado. O sinalizador DEL_ASSOCIATED tem significado apenas para a pasta de nível superior na qual a chamada atua.
    
DELETE_HARD_DELETE
  
> Remove permanentemente todas as mensagens, incluindo as excluídas de forma reversível.
    
FOLDER_DIALOG 
  
> Exibe um indicador de progresso enquanto a operação prossegue.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A pasta foi esvaziada com êxito.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas a pasta não foi completamente esvaziada. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: EmptyFolder** exclui todo o conteúdo de uma pasta sem excluir a pasta propriamente dita. 
  
Durante uma chamada **EmptyFolder** , as mensagens enviadas não são excluídas. 
  
O conteúdo associado de uma pasta inclui mensagens usadas para descrever modos de exibição, regras, formulários personalizados e armazenamento de solução personalizada, e também pode incluir definições de formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não chame o método [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para mensagens na pasta que foi enviada. As mensagens enviadas não são excluídas. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espere estes valores de retorno sob as condições a seguir.
  
|**Condition**|**Valor retornado**|
|:-----|:-----|
|**EmptyFolder** esvaziar a pasta com êxito.  <br/> |S_OK  <br/> |
|**EmptyFolder** não pôde esvaziar completamente a pasta.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Quando o **EmptyFolder** não puder ser concluído, não presuma que nenhum trabalho foi realizado. **EmptyFolder** pode ter sido possível excluir parte do conteúdo da pasta antes de encontrar o erro. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnEmptyFolder  <br/> |MFCMAPI usa o método **IMAPIFolder:: EmptyFolder** para excluir o conteúdo da pasta especificada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

