---
title: xlRunningOnCluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- xlrunningoncluster
localization_priority: Normal
ms.assetid: 7662f255-4184-4af0-97f5-9a89347a201a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f5c630c73899b07e2727a7d42b18eb1891797bab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310098"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna um valor que indica se a função definida pelo usuário está sendo executada em um cluster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Esta função não tem argumentos.
  
## <a name="return-value"></a>Valor de retorno

Se a função estiver em execução em um processo do Excel, retornará 0 em um **XLOPER12** do tipo **xlTypeInt**. Se a função estiver em execução em um cluster, o tipo de retorno e o valor serão determinados pelo provedor do conector de cluster.
  
## <a name="requirements"></a>Requirements

Essa função é definida no arquivo de cabeçalho xlcall. h.
  
## <a name="see-also"></a>Confira também

- [Funções seguras para clusters](cluster-safe-functions.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

