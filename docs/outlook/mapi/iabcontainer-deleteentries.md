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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425593"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove uma ou mais entradas, normalmente usuários de mensagens, listas de distribuição ou outros contêineres.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntries_
  
> [in] Um ponteiro para uma matriz de [estruturas ENTRYLIST](entrylist.md) que contêm identificadores de entrada que representam as entradas que estão sendo excluídas. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As entradas especificadas foram excluídas com êxito. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas uma ou mais entradas não puderam ser excluídas. Quando esse valor é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse valor, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o **método DeleteEntries** para excluir uma entrada específica de um contêiner de um livro de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

