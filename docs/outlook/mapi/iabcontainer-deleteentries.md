---
title: IABContainerDeleteEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.DeleteEntries
api_type:
- COM
ms.assetid: 70a24811-0c41-4b44-8c63-7ef807bc9051
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e3b238129e55e03da33ef3af75ecce7e73fbad03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339379"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove uma ou mais entradas, tipicamente usuários de mensagens, listas de distribuição ou outros contêineres.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntries_
  
> no Um ponteiro para uma matriz de [](entrylist.md) estruturas ENTRYLIST que contêm identificadores de entrada que representam as entradas sendo excluídas. 
    
 _ulFlags_
  
> no Serve deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As entradas especificadas foram excluídas com êxito. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada teve êxito, mas uma ou mais entradas não puderam ser excluídas. Quando esse valor é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse valor, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Abdlg. cpp  <br/> |CabDlg:: OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **DeleteEntries** para excluir uma entrada específica de um contêiner de catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

