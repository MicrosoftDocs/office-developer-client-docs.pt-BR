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
ms.openlocfilehash: babff746af16d51ca154d049943f6be7e9fab589
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428778"
---
# <a name="imapiforminfocalcverbset"></a>IMAPIFormInfo::CalcVerbSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para o conjunto completo de verbos que um formulário usa.
  
```cpp
HRESULT CalcVerbSet(
  ULONG ulFlags,
  LPMAPIVERBARRAY FAR * ppMAPIVerbArray
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo de cadeia de caracteres retornada. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres retornadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _ppMAPIVerbArray_
  
> [out] Um ponteiro para um ponteiro para a estrutura [SMAPIVerbArray](smapiverbarray.md) retornada que contém os verbos do formulário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam o método **IMAPIFormInfo::CalcVerbSet** para obter um ponteiro para o conjunto de verbos usados por um formulário. Na estrutura **SMAPIVerbArray** retornada no parâmetro _ppMAPIVerbArray,_ os verbos são retornados na ordem do número de índice; o índice de cada verbo é encontrado em seu **membro lVerb.** Os aplicativos cliente podem usar a matriz de verbos para criar menus dinamicamente, ocultar ou mostrar botões e assim por diante. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MFCOutput.cpp  <br/> |_OutputFormInfo  <br/> |MFCMAPI usa o **método IMAPIFormInfo::CalcVerbSet** ao escrever a saída de depuração para objetos de informações de formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[SMAPIVerbArray](smapiverbarray.md)
  
[IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

