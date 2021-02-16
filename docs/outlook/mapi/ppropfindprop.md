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
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406336"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Pesquisa uma propriedade especificada em um conjunto de propriedades.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parâmetros

 _rgprop_
  
> [in] Matriz de [estruturas SPropValue](spropvalue.md) que definem as propriedades a serem pesquisadas. 
    
 _cprop_
  
> [in] Contagem de propriedades no conjunto de propriedades indicado pelo _parâmetro rgprop._ 
    
 _ulPropTag_
  
> [in] Marca de propriedade da propriedade a ser pesquisada no conjunto de propriedades indicado pelo _parâmetro rgprop._ 
    
## <a name="return-value"></a>Valor de retorno

 **PpropFindProp** retorna uma [estrutura SPropValue](spropvalue.md) definindo a propriedade que corresponde à marca de propriedade de entrada ou NULL se não houver nenhuma combinação. 
  
## <a name="remarks"></a>Comentários

Se a marca de propriedade determinada indicar uma propriedade do tipo PT_UNSPECIFIED, a função **PpropFindProp** localiza uma combinação apenas para o identificador de propriedade na marca. Caso contrário, ele encontra uma combinação para a marca de propriedade inteira, incluindo o tipo de propriedade, e retorna a propriedade identificada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI usa o **método PpropFindProp** para encontrar propriedades em um conjunto de propriedades sendo adicionado à lista.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

