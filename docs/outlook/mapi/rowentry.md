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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436031"
---
# <a name="rowentry"></a>ROWENTRY

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma linha e a operação que é executada nessa linha em uma tabela por meio da interface [IExchangeModifyTable.](iexchangemodifytableiunknown.md) 
  
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
  
> Uma das seguintes operações a serem executadas nos dados: 
    
  - ROW_ADD: adicione os dados à tabela como uma nova linha.
      
  - ROW_MODIFY: modifique esta linha na tabela.
      
  - ROW_REMOVE: remova esta linha da tabela.
      
  - ROW_EMPTY: não adicione os dados de linha à tabela. (A linha está vazia.)
    
**cValues**
  
> O número de valores de propriedade **em rgPropvals**.
    
**rgPropVals**
  
> Uma matriz de [estruturas SPropValue](spropvalue.md) que representam os valores de colunas a serem inseridos na tabela. 
    
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Usado para criar uma lista de regras selecionadas para ações **ModifyTable** subsequentes.  <br/> |
   
## <a name="see-also"></a>Confira também
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Estruturas MAPI](mapi-structures.md)

