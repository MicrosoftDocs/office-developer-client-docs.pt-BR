---
title: ROWENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ROWENTRY
api_type:
- COM
ms.assetid: bd6c0d8e-68cc-4d60-9029-13ed81c816cd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 243ab1e926171ee66b95cfd8e969cd77e2b31faf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279598"
---
# <a name="rowentry"></a>ROWENTRY

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma linha e a operação que é executada nessa linha em uma tabela através da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
```cpp
typedef struct
{
  ULONG         ulRowFlags;
  ULONG         cValues;
  LPSPropValue  rgPropVals;
}  ROWENTRY, FAR * LPROWENTRY;
```

## <a name="members"></a>Members

**ulRowFlags**
  
> Uma das operações a seguir a ser executada nos dados: 
    
  - ROW_ADD: adicionar os dados à tabela como uma nova linha.
      
  - ROW_MODIFY: modifique essa linha na tabela.
      
  - ROW_REMOVE: remova essa linha da tabela.
      
  - ROW_EMPTY: Não adicione os dados da linha à tabela. (A linha está vazia.)
    
**cValues**
  
> O número de valores de propriedade em **rgPropvals**.
    
**rgPropVals**
  
> Uma matriz de estruturas [SPropValue](spropvalue.md) que representa os valores das colunas a serem inseridas na tabela. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|RulesDlg. cpp  <br/> |CRulesDlg:: getSelectedItems  <br/> |Usado para criar uma lista de regras selecionadas para ações **modificadas** subsequentes.  <br/> |
   
## <a name="see-also"></a>Confira também
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Estruturas MAPI](mapi-structures.md)

