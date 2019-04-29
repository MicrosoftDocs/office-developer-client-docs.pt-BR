---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415653"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica em que local da mensagem um segmento de mensagem pertence. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a>Parâmetros

 _cbParent_
  
> no Contagem de bytes no índice de conversa pai.
    
 _lpbParent_
  
> no Ponteiro para bytes no índice de conversa pai. Isso pode ser NULL se _cbParent_ for zero. 
    
 _lpcbIndex_
  
> bota Ponteiro para a contagem de bytes no novo índice de conversa retornado pela chamada. 
    
 _lppbIndex_
  
> bota Ponteiro para um ponteiro para o novo índice de conversa retornado pela chamada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    

