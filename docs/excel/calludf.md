---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 096f57335572c3788fdf129dd3bcf4a76cf62b01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433007"
---
# <a name="calludf"></a>CallUDF

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função definida pelo usuário em um ambiente de computação de alto desempenho.
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>Parâmetros

_Identificação_da_sessão_
  
> A ID da sessão na qual a chamada será feita.
    
_XLLName_
  
> O nome do XLL que contém a função definida pelo usuário.
    
_UDFName_
  
> O nome da função definida pelo usuário.
    
_CallBackAddr_
  
> A função que o conector deve chamar quando a função definida pelo usuário estiver concluída.
    
_pxAsyncHandle_
  
> O identificador assíncrono usado pelo Excel e o conector para rastrear a chamada de função definida pelo usuário pendente. O conector o utiliza posteriormente quando a chamada for concluída, quando ele chamar de volta para o Excel usando o ponteiro de função passado no argumento _CallBackAddr_ . 
    
_ArgCount_
  
> O número de argumentos a serem passados para a função definida pelo usuário. O valor máximo permitido é 255.
    
_Parâmetro1_
  
> Um valor a ser passado para a função definida pelo usuário. Repita esse argumento para cada parâmetro indicado por _ArgCount_.
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se a chamada UDF for iniciada com êxito; **xlHpcRetInvalidSessionId** se o argumento _SessionID_ for inválido; **xlHpcRetCallFailed** em outras falhas, incluindo o tempo limite. Se a chamada retornar qualquer código de erro (qualquer coisa exceto **xlHpcRetSuccess**), o Excel considerará a chamada UDF para ter falhado, invalidará o _pxAsyncHandle_e não esperará que um retorno de chamada ocorra.
  
## <a name="remarks"></a>Comentários

Essa função é executada de forma assíncrona.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

