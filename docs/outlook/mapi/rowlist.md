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
ms.openlocfilehash: d0427e36d07d1cdc4f88e471f9ca006e737b73f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770279"
---
# <a name="rowlist"></a>ROWLIST

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas [ROWENTRY](rowentry.md) representando as linhas e as operações que são executadas nessas linhas em uma tabela por meio da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
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
  
> Matriz de estruturas **ROWENTRY** que contém as linhas e as operações que são realizadas nessas linhas da tabela. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Usado para criar uma lista das regras selecionadas para ações de **ModifyTable** subsequentes.  <br/> |
   
## <a name="see-also"></a>Confira também



[ROWENTRY](rowentry.md)
  
[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Estruturas MAPI](mapi-structures.md)

