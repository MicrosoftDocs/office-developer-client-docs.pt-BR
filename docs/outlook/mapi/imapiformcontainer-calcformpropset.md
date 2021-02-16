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
  
Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulário.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppResults
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como a matriz de propriedades no  _parâmetro ppResults_ é retornada. Os sinalizadores a seguir podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção das propriedades dos formulários.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a união das propriedades dos formulários.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppResults_
  
> [out] Um ponteiro para um ponteiro para a estrutura [SMAPIFormPropArray](smapiformproparray.md) retornada. Essa estrutura contém todas as propriedades usadas pelos formulários instalados. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormContainer::CalcFormPropSet** para obter uma matriz de propriedades usadas por todos os formulários instalados em um contêiner de formulário. **IMAPIFormContainer::CalcFormPropSet** funciona como o método [IMAPIFormMgr::CalcFormPropSet,](imapiformmgr-calcformpropset.md) exceto que ele opera em todos os formulário registrados em um contêiner específico. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Provedores de biblioteca de formulário que não suportam cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE for passado.
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPIFormContainer::CalcFormPropSet** aceita uma interseção ou uma união dos conjuntos de propriedades dos formulários, dependendo do sinalizador definido no parâmetro  _ulFlags,_ e retorna uma estrutura **SMAPIFormPropArray** que contém o grupo de propriedades resultante. 
  
Se um cliente passar o sinalizador MAPI_UNICODE  _ulFlags_, todas as cadeias de caracteres retornadas serão Unicode.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

