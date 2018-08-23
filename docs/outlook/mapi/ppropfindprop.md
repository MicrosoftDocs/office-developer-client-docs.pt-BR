---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f720160193613bbbb4bbd447f78c14e6e5378eb8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565652"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Procura uma propriedade especificada em uma propriedade definida.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _rgprop_
  
> [in] Matriz de estruturas de [SPropValue](spropvalue.md) que definem as propriedades a serem pesquisados. 
    
 _cprop_
  
> [in] Contagem de propriedades no conjunto de propriedade indicada pelo parâmetro _rgprop_ . 
    
 _ulPropTag_
  
> [in] Marca de propriedade para a propriedade pesquisar no conjunto de propriedades indicado pelo parâmetro _rgprop_ . 
    
## <a name="return-value"></a>Valor retornado

 **PpropFindProp** retorna uma estrutura de [SPropValue](spropvalue.md) definindo a propriedade que corresponda a propriedade input marca ou NULL se não houver nenhuma correspondência. 
  
## <a name="remarks"></a>Comentários

Se a marca de propriedade determinado indica uma propriedade do tipo PT_UNSPECIFIED, a função **PpropFindProp** localiza uma correspondência apenas para o identificador de propriedade da marca. Caso contrário, ele encontra uma correspondência para a marca de propriedade inteira, incluindo o tipo de propriedade e retorna a propriedade identificada. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI usa o método **PpropFindProp** para localizar propriedades em uma propriedade definidas que está sendo adicionado à lista.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

