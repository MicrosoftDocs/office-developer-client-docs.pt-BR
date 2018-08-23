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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9c6a6d210230fc305aef46371c22f67b3d445a81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576579"
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
  
> [in] Uma bitmask dos sinalizadores que controla como a matriz de propriedade no parâmetro _ppResults_ é retornada. Sinalizadores a seguir podem ser definidos: 
    
FORMPROPSET_INTERSECTION 
  
> A matriz retornada contém a interseção de propriedades dos formulários.
    
FORMPROPSET_UNION 
  
> A matriz retornada contém a união de propriedades dos formulários.
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas na matriz estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppResults_
  
> [out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado. Essa estrutura contém todas as propriedades usadas pelos formulários instalados. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método de **IMAPIFormContainer::CalcFormPropSet** para obter uma matriz de propriedades usadas por todos os formulários instalados em um contêiner de formulário. **IMAPIFormContainer::CalcFormPropSet** funciona como o método [IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md) , exceto que ele opera em todos os formulários registrado em um contêiner específico. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Provedores de biblioteca de formulário que não oferecem suporte a cadeias de caracteres Unicode devem retornar MAPI_E_BAD_CHARWIDTH se MAPI_UNICODE é passado.
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **IMAPIFormContainer::CalcFormPropSet** utiliza uma interseção ou uma união de conjuntos de propriedades dos formulários, dependendo do sinalizador definido no parâmetro _ulFlags_ , e ele retorna uma estrutura **SMAPIFormPropArray** que contém o grupo resultante de propriedades. 
  
Se um cliente passa o sinalizador MAPI_UNICODE em _ulFlags_, todas as cadeias de caracteres retornadas são Unicode.
  
## <a name="see-also"></a>Confira também



[IMAPIFormMgr::CalcFormPropSet](imapiformmgr-calcformpropset.md)
  
[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)

