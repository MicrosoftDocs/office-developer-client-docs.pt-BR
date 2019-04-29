---
title: IMAPIFormContainerCalcFormPropSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.CalcFormPropSet
api_type:
- COM
ms.assetid: 594e3aac-a00f-422e-8e7a-949e4c9a3f8d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ec1933f80f211c7c381f9de6b15d414932b9a78e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414911"
---
# <a name="imapiformcontainercalcformpropset"></a>IMAPIFormContainer::CalcFormPropSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulários.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a matriz de propriedades no parâmetro _ppResults_ é retornada. Os seguintes sinalizadores podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção das propriedades de formulários.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a União das propriedades dos formulários.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _ppResults_
  
> bota Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada. Esta estrutura contém todas as propriedades usadas pelos formulários instalados. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer:: CalcFormPropSet** para obter uma matriz de propriedades usadas por todos os formulários instalados em um contêiner de formulários. **IMAPIFormContainer:: CalcFormPropSet** funciona como o método [IMAPIFormMgr:: CalcFormPropSet](imapiformmgr-calcformpropset.md) , exceto pelo fato de que ele opera em todos os formulários registrados em um contêiner específico. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os provedores de biblioteca de formulários que não dão suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPIFormContainer:: CalcFormPropSet** assume uma interseção ou uma União dos conjuntos de propriedades de formulários, dependendo do sinalizador definido no parâmetro _parâmetroulflags_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de propriedades. 
  
Se um cliente passar o sinalizador MAPI_UNICODE no _parâmetroulflags_, todas as cadeias de caracteres retornadas serão Unicode.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

