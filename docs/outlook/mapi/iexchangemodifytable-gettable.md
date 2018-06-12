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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0cf9373c68d533908b857a4d8f1c0e71aa11846f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766934"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Aplica-se a**: Outlook 
  
Retorna um ponteiro para uma interface para um objeto table MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Reservado; deve ser 0 (zero).
    
ACLTABLE_FREEBUSY
  
> Define o novos direitos.
    
frightsFreeBusyDetailed
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada das novas direitos de livre/ocupado.
    
frightsFreeBusySimple
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simple de novos direitos de livre/ocupado.
    
 _lppTable_
  
> [out] Aponta para um [IMAPITable: IUnknown](imapitableiunknown.md) interface que contém o objeto table. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI usa o método **IExchangeModifyTable::GetTable** para obter uma tabela de regras.  <br/> |
   
## <a name="see-also"></a>Confira também



[IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

