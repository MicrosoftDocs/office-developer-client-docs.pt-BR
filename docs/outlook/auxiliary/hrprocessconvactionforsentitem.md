---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Executa pós-enviar categorização em um item de email com base em sua PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765823"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Executa pós-enviar categorização em um item de email com base em suas [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportá-los por:  <br/> |Outlook.exe  <br/> |
|Chamado pelo:  <br/> |Cliente  <br/> |
|Implementada por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parâmetros

_pmbinStoreEid_
  
> [in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do repositório ou o [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) do item de email. Não pode ser NULL ou inválidas. 
    
_pmbinMsgEid_
  
> [in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do item de email. Não pode ser NULL ou inválidas. 
    
_pmbinConvID_
  
> [in] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) do item de email. Não pode ser NULL ou inválidas. 
    
_dwFlags_
  
> [in] Uma máscara de bits que especifica informações adicionais sobre a chamada de método.
    
   - 0 – há opções adicionais são usadas nessa chamada de método. Este é o valor recomendado. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ é realmente o [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) da mensagem. Usando um **PidTagSearchKey** faz uso de recursos e deve ser evitado se um [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) estiver disponível. 
    
## <a name="return-values"></a>Valores de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ contém um sinalizador desconhecido.  <br/> |
   
## <a name="remarks"></a>Comentários

Categorias são consideradas informações pessoais e não devem ser transmitidas fora da caixa de correio do usuário. Portanto, não chame **HrProcessConvActionForSentItem** em um item de email não enviados. Em vez disso, enviar o item e, em seguida, chame **HrProcessConvActionForSentItem** na cópia arquivada. A cópia arquivada pode ser armazenada na pasta Itens enviados, ou um local equivalente. 
  
Seu aplicativo deve ser em processo com Outlook.exe, tais como um suplemento COM, chamar **HrProcessConvActionForSentItem**. Se você tentar chamar fora do processo **HrProcessConvActionForSentItem** , **HrProcessConvActionForSentItem** lançará uma exceção de violação de acesso. 
  

