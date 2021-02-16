---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Executa a categorização pós-envio em um item de email com base na sua PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318897"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

Executa a categorização pós-envio em um item de email com base na sua [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Exportado por:  <br/> |Outlook.exe  <br/> |
|Chamado por:  <br/> |Cliente  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>Parâmetros

_pmbinStoreEid_
  
> [in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do repositório ou [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) do item de email. Não pode ser nulo ou inválido. 
    
_pmbinMsgEid_
  
> [in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) do item de email. Não pode ser nulo ou inválido. 
    
_pmbinConvID_
  
> [in] [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) do item de email. Não pode ser nulo ou inválido. 
    
_dwFlags_
  
> [in] Um bitmask que especifica informações adicionais sobre a chamada do método.
    
   - 0—Nenhuma opção adicional é usada nesta chamada de método. Esse é o valor recomendado. 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ é na verdade o [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) da mensagem. Usar **PidTagSearchKey** é um recurso intensivo e deve ser evitado se [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) estiver disponível. 
    
## <a name="return-values"></a>Valor de retorno

|**HRESULT**|**Descrição**|
|:-----|:-----|
|S_OK  <br/> |A chamada foi bem-sucedida.  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_ contém um sinalizador desconhecido.  <br/> |
   
## <a name="remarks"></a>Comentários

As categorias são consideradas informações pessoais e não devem ser transmitidas fora da caixa de correio do usuário. Portanto, não chame **HrProcessConvActionForSentItem** em um item de email não enviado. Em vez disso, envie o item e, em seguida, chame **HrProcessConvActionForSentItem** na cópia arquivada. A cópia arquivada pode ser armazenada na pasta Itens enviados ou em um local equivalente. 
  
Seu aplicativo deve estar em processo com o Outlook.exe, como de um suplemento COM, para chamar **HrProcessConvActionForSentItem**. Se você tentar chamar **HrProcessConvActionForSentItem** fora do processo, **HrProcessConvActionForSentItem** lançará uma exceção de violação de acesso. 
  

