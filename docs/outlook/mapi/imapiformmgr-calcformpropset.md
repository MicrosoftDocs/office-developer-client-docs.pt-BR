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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342081"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma matriz das propriedades usadas por um grupo de formulários.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parâmetros

 _pfrminfoarray_
  
> no Um ponteiro para uma matriz de objetos de informação de formulário que identificam os formulários para os quais retornar propriedades.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a matriz de propriedades no parâmetro _ppResults_ é retornada. Os seguintes sinalizadores podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção das propriedades do formulário.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a União das propriedades do formulário.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _ppResults_
  
> bota Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada, que contém as propriedades que os formulários utilizam. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

Os visualizadores de formulários chamam o método **IMAPIFormMgr:: CalcFormPropSet** para obter uma matriz das propriedades usadas por um grupo de formulários. O **CalcFormPropSet** utiliza uma interseção ou uma União desses conjuntos de propriedades de formulários, dependendo do sinalizador definido no parâmetro _parâmetroulflags_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de Propriedades. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se um visualizador de formulários passar o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ , todas as cadeias de caracteres deverão ser retornadas como cadeias de caracteres Unicode. Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="see-also"></a>Confira também



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

