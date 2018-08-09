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
ms.openlocfilehash: 15cf8ff7e282035ddff53565aa92e81e3886729c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766962"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da subpasta para excluir.
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai do indicador de progresso. O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador FOLDER_DIALOG é definido no parâmetro _ulFlags_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador FOLDER_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla a exclusão da subpasta. Sinalizadores a seguir podem ser definidos:
    
DEL_FOLDERS 
  
> Todas as subpastas da subpasta apontado pela _lpEntryID_ devem ser excluídas. 
    
DEL_MESSAGES 
  
> Todas as mensagens na subpasta apontado pela _lpEntryID_ devem ser excluídas. 
    
FOLDER_DIALOG 
  
> Um indicador de progresso deve ser exibido enquanto continua a operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A pasta especificada foi excluída com êxito.
    
MAPI_E_HAS_FOLDERS 
  
> A subpasta que está sendo excluída contém subpastas e o sinalizador DEL_FOLDERS não foi definido. As subpastas não foram excluídas.
    
MAPI_E_HAS_MESSAGES 
  
> A subpasta que está sendo excluída contém mensagens e o sinalizador DEL_MESSAGES não foi definido. A subpasta não foi excluída.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram excluídas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::DeleteFolder** exclui uma subpasta. Por padrão, **DeleteFolder** opera somente em pastas vazias, mas você pode usá-lo com êxito em pastas não vazias definindo dois sinalizadores: DEL_FOLDERS e DEL_MESSAGES. Apenas pastas vazias ou pastas que definir sinalizadores DEL_FOLDERS tanto o DEL_MESSAGES na chamada **DeleteFolder** podem ser excluídas. DEL_FOLDERS habilita todas as subpastas da pasta a ser removida; DEL_MESSAGES habilita todas as mensagens da pasta a ser removida. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Quando a operação de exclusão envolve mais de uma pasta, execute a operação como completamente para cada pasta. Em alguns casos, uma das pastas a ser excluído não existe ou foi movida ou copiada em outro local. Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**DeleteFolder** excluiu com êxito cada mensagem e a subpasta.  <br/> |S_OK  <br/> |
|**DeleteFolder** não pôde ser excluído com êxito a cada mensagem e a subpasta.  <br/> |MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND  <br/> |
|**DeleteFolder** não pôde concluir.  <br/> |Qualquer valor de erro, exceto E_NOT_FOUND  <br/> |
   
Quando **DeleteFolder** é impossível concluir, não presuma que foi feito nenhum trabalho. **DeleteFolder** podem ter sido capazes de excluir uma ou mais das mensagens e subpastas antes da ocorrência de erro. 
  
Se uma ou mais subpastas não podem ser excluídas, **DeleteFolder** retorna MAPI_W_PARTIAL_COMPLETION ou E_NOT_FOUND, dependendo da implementação do provedor de repositório de mensagem. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **IMAPIFolder::DeleteFolder** para excluir pastas.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

