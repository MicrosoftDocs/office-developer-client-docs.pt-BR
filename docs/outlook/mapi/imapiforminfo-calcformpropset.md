---
title: IMAPIFormInfoCalcFormPropSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.CalcFormPropSet
api_type:
- COM
ms.assetid: cc3ffb8d-9cc4-47d3-9aa9-02c3a5b7775c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e5da9ffdd3021538ec814d1367cf1b06b49cfbc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767022"
---
# <a name="imapiforminfocalcformpropset"></a>IMAPIFormInfo::CalcFormPropSet

  
  
**Aplica-se a**: Outlook 
  
Retorna um ponteiro para o conjunto completo de propriedades que usa um formulário.
  
```cpp
HRESULT CalcFormPropSet(
  ULONG ulFlags,
  LPMAPIFORMPROPARRAY FAR * ppFormPropArray
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de cadeias de caracteres retornada. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppFormPropArray_
  
> [out] Um ponteiro para um ponteiro para a estrutura de [SMAPIFormPropArray](smapiformproparray.md) retornado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI usa o método de **IMAPIFormInfo::CalcFormPropSet** durante a criação de saída de depuração para os objetos de informações do formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[SMAPIFormPropArray](smapiformproparray.md)
  
[IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

