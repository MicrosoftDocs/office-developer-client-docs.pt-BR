---
title: IMAPIFormMgrCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CalcFormPropSet
api_type:
- COM
ms.assetid: ab302bfd-5cff-49b4-b0d2-308ae5af478d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf072aba27c90b7cea80c464e17fafb47524b695
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436423"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma matriz das propriedades que um grupo de formulários usa.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parâmetros

 _pfrminfoarray_
  
> [in] Um ponteiro para uma matriz de objetos de informações de formulário que identificam os formulários para os quais retornar propriedades.
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como a matriz de propriedades no  _parâmetro ppResults_ é retornada. Os sinalizadores a seguir podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção das propriedades do formulário.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a união das propriedades do formulário.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppResults_
  
> [out] Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada, que contém as propriedades que os formulários usam. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIFormMgr::CalcFormPropSet** para obter uma matriz das propriedades que um grupo de formulários usa. **CalcFormPropSet** assume uma interseção ou uma união dos conjuntos de propriedades desses formulários, dependendo do sinalizador definido no parâmetro  _ulFlags,_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo de propriedades resultante. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um visualizador de formulário passar o sinalizador MAPI_UNICODE no parâmetro  _ulFlags,_ todas as cadeias de caracteres deverão ser retornadas como cadeias de caracteres Unicode. Provedores de biblioteca de formulário que não suportam cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE for passado. 
  
## <a name="see-also"></a>Confira também



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

