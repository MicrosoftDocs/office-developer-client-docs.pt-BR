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
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578987"
---
# <a name="iexchangemodifytablegettable"></a>IExchangeModifyTable::GetTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para uma interface para um objeto table MAPI.
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a>Parâmetros

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



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

