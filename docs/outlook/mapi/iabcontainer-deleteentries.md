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
ms.openlocfilehash: 4140dc39b7f866b0372e5940aef5efc0524ad593
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573107"
---
# <a name="iabcontainerdeleteentries"></a>IABContainer::DeleteEntries

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove uma ou mais entradas, normalmente mensagens outros contêineres, listas de distribuição ou os usuários.
  
```cpp
HRESULT DeleteEntries(
  LPENTRYLIST lpEntries,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpEntries_
  
> [in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que contêm os identificadores de entrada que representam as entradas que está sendo excluídas. 
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As entradas especificadas tenham sido excluídas com êxito. 
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas um ou mais das entradas não pôde ser excluída. Quando este valor é retornado, a chamada deve ser manipulada com êxito. Para testar esse valor, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|Abdlg.cpp  <br/> |CabDlg::OnDeleteSelectedItem  <br/> |MFCMAPI usa o método **DeleteEntries** para excluir uma entrada específica de um contêiner de catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

