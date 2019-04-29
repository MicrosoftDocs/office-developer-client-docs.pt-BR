---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436241"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para uma interface de um objeto MAPI da tabela.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser 0 (zero).
    
ACLTABLE_FREEBUSY
  
> Define novos direitos.
    
frightsFreeBusyDetailed
  
> Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada dos novos direitos de disponibilidade.
    
frightsFreeBusySimple
  
> Quando o ACLTABLE_FREEBUSY é passado, fornece uma exibição simples de novos direitos de disponibilidade.
    
 _lppTable_
  
> bota Aponta para uma interface imApitable [: IUnknown](imapitableiunknown.md) contendo o objeto Table. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: OnRefreshView  <br/> |MFCMAPI usa o método **IExchangeModifyTable:: GetTable** para obter uma tabela de regras.  <br/> |
   
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

