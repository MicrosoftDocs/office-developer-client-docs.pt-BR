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

_SessionId_
  
> A ID da sessão na qual fazer a chamada.
    
_XLLName_
  
> O nome da XLL que contém a função definida pelo usuário.
    
_UDFName_
  
> O nome da função definida pelo usuário.
    
_CallBackAddr_
  
> A função que o conector deve chamar quando a função definida pelo usuário for concluída.
    
_pxAsyncHandle_
  
> O alça assíncrona usada pelo Excel e pelo conector para controlar a chamada de função pendente definida pelo usuário. O conector o usa mais tarde quando a chamada é concluída, quando ele chama de volta para o Excel usando o ponteiro de função passado no _argumento CallBackAddr._ 
    
_ArgCount_
  
> O número de argumentos a passar para a função definida pelo usuário. O valor máximo permitido é 255.
    
_Parameter1_
  
> Um valor a ser aprovado para a função definida pelo usuário. Repita esse argumento para cada parâmetro indicado por  _ArgCount_.
    
## <a name="return-value"></a>Valor de retorno

**xlHpcRetSuccess** se a chamada UDF for iniciada com êxito; **xlHpcRetInvalidSessionId** se o  _argumento SessionId_ for inválido; **xlHpcRetCallFailed** em outras falhas, incluindo tempo o tempo exemportado. Se a chamada retornar qualquer código de erro (qualquer coisa exceto **xlHpcRetSuccess**), o Excel considerará que a chamada UDF falhou, invalida o  _pxAsyncHandle_ e não espera que ocorra um retorno de chamada.
  
## <a name="remarks"></a>Comentários

Essa função é executada de forma assíncrona.
  
## <a name="see-also"></a>Confira também

- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)

