---
title: IMAPIFormInfoCalcVerbSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcVerbSet
api_type:
- COM
ms.assetid: 0170dc9d-dc72-48e2-a522-374f199b18ea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db3cc987b20a76116f2591485f57afae017d3e15
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567710"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para o conjunto completo de verbos que usa um formulário.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppMAPIVerbArray_
  
> [out] Um ponteiro para um ponteiro para a estrutura [SMAPIVerbArray](smapiverbarray.md) retornado que contém os verbos do formulário. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="remarks"></a>Comentários

Aplicativos cliente chamam o método **IMAPIFormInfo::CalcVerbSet** para obter um ponteiro para o conjunto de verbos usado por um formulário. Na estrutura de **SMAPIVerbArray** retornada no parâmetro _ppMAPIVerbArray_ , os verbos são retornados em ordem de número de índice; índice da cada verbo é encontrado na sua lista de membros **lVerb** . Aplicativos cliente podem usar a matriz de verbo para dinamicamente construir menus, ocultar ou Mostrar botões e assim por diante. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI usa o método de **IMAPIFormInfo::CalcVerbSet** ao gravar a saída de depuração para os objetos de informações do formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

