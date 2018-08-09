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
ms.openlocfilehash: f42ccbeb94e1fc6b6cf880f1b32ee1bfeb24997e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765501"
---
# <a name="xlrunningoncluster"></a>xlRunningOnCluster

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna um valor que indica se a função definida pelo usuário está sendo executado em um cluster. 
  
```cpp
Excel12(xlRunningOnCluster, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem argumentos.
  
## <a name="return-value"></a>Valor retornado

Se a função estiver em execução em um processo de Excel, retornará 0 no **XLOPER12** do tipo **xlTypeInt**. Se a função estiver em execução em um cluster, o tipo de retorno e o valor é determinado pelo provedor de conector de cluster.
  
## <a name="requirements"></a>Requisitos

Esta função é definida no arquivo de cabeçalho xlcall. h.
  
## <a name="see-also"></a>Confira também

- [Funções de segurança do cluster](cluster-safe-functions.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

