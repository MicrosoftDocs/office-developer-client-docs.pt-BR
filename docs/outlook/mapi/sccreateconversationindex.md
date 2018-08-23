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
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594143"
---
# <a name="sccreateconversationindex"></a>ScCreateConversationIndex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica onde em um segmento de mensagem uma mensagem pertence. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Contagem de bytes no índice de conversa pai.
    
 _lpbParent_
  
> [in] Ponteiro para bytes no índice de conversa pai. Isso pode ser NULL se _cbParent_ for zero. 
    
 _lpcbIndex_
  
> [out] Ponteiro para a contagem de bytes no índice da nova conversa retornado pela chamada. 
    
 _lppbIndex_
  
> [out] Ponteiro para um ponteiro para o novo índice de conversação retornado pela chamada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    

