---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565904"
---
# <a name="iexchangemodifytablemodifytable"></a>IExchangeModifyTable::ModifyTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Atualiza um objeto table MAPI.
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Use um dos seguintes valores: 
    
0 (zero)
  
> Use o valor do membro **ulRowFlags** da estrutura [ROWENTRY](rowentry.md) . 
    
ACLTABLE_FREEBUSY
  
> Define o novos direitos.
    
frightsFreeBusyDetailed
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição detalhada das novas direitos de livre/ocupado.
    
frightsFreeBusySimple
  
> Quando ACLTABLE_FREEBUSY é passado, fornece uma exibição simple de novos direitos de livre/ocupado.
    
ROWLIST_REPLACE
  
> Substitua todas as linhas na tabela.
    
 _lpMods_
  
> [in] Aponta para uma estrutura [ROWLIST](rowlist.md) que contém as propriedades para o objeto table. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::OnModifySelectedItem  <br/> |MFCMAPI usa o método **IExchangeModifyTable::ModifyTable** para gravar uma regra modificada de volta à tabela de regras.  <br/> |
   
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[ROWENTRY](rowentry.md)
  
[ROWLIST](rowlist.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

