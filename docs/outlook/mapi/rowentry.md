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
ms.openlocfilehash: f8ac73b1977886208290285fec2d1bd0de1b4f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770281"
---
# <a name="rowentry"></a>ROWENTRY

**Aplica-se a**: Outlook 
  
Contém uma linha e a operação é realizada nessa linha em uma tabela por meio da interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) . 
  
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
    
  - ROW_ADD: Adicione os dados à tabela como uma nova linha.
      
  - ROW_MODIFY: Modifica essa linha da tabela.
      
  - ROW_REMOVE: Remova essa linha da tabela.
      
  - ROW_EMPTY: Não adicione os dados de linha à tabela. (A linha estará vazia).
    
**cValues**
  
> O número de valores de propriedade em **rgPropvals**.
    
**rgPropVals**
  
> Uma matriz de estruturas de [SPropValue](spropvalue.md) que representam os valores de colunas a ser inserido na tabela. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|RulesDlg.cpp  <br/> |CRulesDlg::GetSelectedItems  <br/> |Usado para criar uma lista das regras selecionadas para ações de **ModifyTable** subsequentes.  <br/> |
   
## <a name="see-also"></a>Confira também
  
- [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
- [Estruturas MAPI](mapi-structures.md)

