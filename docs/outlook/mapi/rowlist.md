---
title: ROWLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWLIST
api_type:
- COM
ms.assetid: ce0be0d5-4962-4d53-828f-c93d1c5aae32
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c13b741b1e0ddfd964b9325d736a26dac4bff2af
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419181"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de [](rowentry.md) estruturas de transentry que representam linhas e as operações realizadas em uma tabela através da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG     cEntries;
  ROWENTRY  aEntries[MAPI_DIM];
}  ROWLIST, FAR * LPROWLIST;

```

## <a name="members"></a>Members

 **cEntries**
  
> Contagem de entradas na matriz especificada pelo membro **aEntries** . 
    
 **aEntries [MAPI_DIM]**
  
> Matriz de **** estruturas de transentry que contém as linhas e as operações que são executadas nessas linhas na tabela. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: getSelectedItems  <br/> |Usado para criar uma lista de regras selecionadas para ações **modificadas** subsequentes.  <br/> |
   
## <a name="see-also"></a>Confira também



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Estruturas MAPI](mapi-structures.md)

