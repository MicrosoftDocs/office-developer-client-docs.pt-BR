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
  
Retorna um ponteiro para uma interface para um objeto de tabela MAPI.
  
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
  
> Define novos direitos.
    
freeBusyDetailed
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada dos novos direitos de livre/ocupado.
    
freeBusySimple
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simples de novos direitos de livre/ocupado.
    
 _lppTable_
  
> [out] Aponta para [uma IMAPITable : interface IUnknown](imapitableiunknown.md) que contém o objeto table. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnRefreshView  <br/> |MFCMAPI usa o **método IExchangeModifyTable::GetTable** para obter uma tabela de regras.  <br/> |
   
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

