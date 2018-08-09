---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765253"
---
# <a name="calludf"></a>CallUDF

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função definida pelo usuário em um ambiente de computação de alto desempenho.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parâmetros

_SessionId_
  
> A identificação da sessão em que deseja que a chamada.
    
_XLLName_
  
> O nome da XLL que contém a função definida pelo usuário.
    
_UDFName_
  
> O nome da função definida pelo usuário.
    
_CallBackAddr_
  
> A função que o conector deve chamar quando termina a função definida pelo usuário.
    
_pxAsyncHandle_
  
> O identificador assíncrona usado pelo Excel e o conector para controlar a chamada pendente de função definida pelo usuário. O conector usa mais tarde quando a chamada for concluída, quando ele chama de volta para o Excel usando o ponteiro de função passados no argumento _CallBackAddr_ . 
    
_ArgCount_
  
> O número de argumentos a serem passados para a função definida pelo usuário. O valor máximo permitido é 255.
    
_Parâmetro1_
  
> Um valor para passar para a função definida pelo usuário. Repita este argumento para cada parâmetro indicado pelo _ArgCount_.
    
## <a name="return-value"></a>Valor retornado

**xlHpcRetSuccess** se a chamada UDF é iniciada com êxito; **xlHpcRetInvalidSessionId** se o argumento _SessionId_ é inválido; **xlHpcRetCallFailed** em outras falhas, incluindo o tempo limite. Se a chamada retornar qualquer código de erro (nada, exceto **xlHpcRetSuccess**), em seguida, Excel considera que a chamada UDF para ter falhado, invalida o _pxAsyncHandle_e não esperar que ocorra um retorno de chamada.
  
## <a name="remarks"></a>Comentários

Esta função executa de forma assíncrona.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

