---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579309"
---
# <a name="smapiformproparray"></a>SMAPIFormPropArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas de [SMAPIFormProp](smapiformprop.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
|Macro relacionada:  <br/> |[CbMAPIFormPropArray](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a>Members

 **cProps**
  
> Contagem de propriedades nomeadas na matriz no membro **aFormProp** . 
    
 **ulPad**
  
>  Oito bytes de preenchimento usados para garantir o alinhamento correto. 
    
 **aFormProp**
  
> Matriz de propriedades do formulário.
    
## <a name="remarks"></a>Comentários

A estrutura **SMAPIFormPropArray** é passada como um parâmetro para os seguintes métodos: 
  
- [IMAPIFormInfo::CalcFormPropSet](imapiforminfo-calcformpropset.md)
    
- [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
    
- [IMAPIFormContainer::CalcFormPropSet](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a>Confira também



[CbMAPIFormPropArray](cbmapiformproparray.md)
  
[SMAPIFormProp](smapiformprop.md)


[Estruturas MAPI](mapi-structures.md)

