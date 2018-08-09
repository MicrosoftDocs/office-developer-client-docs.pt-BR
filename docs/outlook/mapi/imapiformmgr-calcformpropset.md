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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: abd2a3e2a1a810f902ad977413c89f2e8b0113a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767031"
---
# <a name="imapiformmgrcalcformpropset"></a>IMAPIFormMgr::CalcFormPropSet

  
  
**Aplica-se a**: Outlook 
  
Retorna uma matriz das propriedades que usa um grupo de formulários.
  
```cpp
HRESULT CalcFormPropSet(
  LPSMAPIFORMINFOARRAY pfrminfoarray,
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parâmetros

 _pfrminfoarray_
  
> [in] Um ponteiro para uma matriz de objetos de informações de formulário que identificam os formulários para o qual retornar propriedades.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a matriz de propriedade no parâmetro _ppResults_ é retornada. Sinalizadores a seguir podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção de propriedades do formulário.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a união de propriedades do formulário.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppResults_
  
> [out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado, que contém as propriedades que usam os formulários. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamar o método **IMAPIFormMgr::CalcFormPropSet** para obter uma matriz das propriedades que usa um grupo de formulários. **CalcFormPropSet** leva a uma interseção ou uma união de propriedade desses formulários define, dependendo do sinalizador definido no parâmetro _ulFlags_ e ele retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de Propriedades. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se um visualizador de formulário passa o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ , todas as cadeias de caracteres devem ser retornadas como sequências de caracteres Unicode. Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado. 
  
## <a name="see-also"></a>Confira também



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

