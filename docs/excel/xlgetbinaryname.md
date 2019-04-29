---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- função xlgetbinaryname [Excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412461"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para retornar um identificador para dados salvos pela [função xlDefineBinaryName](xldefinebinaryname.md). Os dados com um nome binário definido são salvos com a pasta de trabalho e podem ser acessados pelo nome a qualquer momento. Para saber mais, confira "limitação de escopo de nome binário" em [problemas conhecidos no desenvolvimento XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parâmetros

_pxRes_ (**xltypeBigData** ou **xltypeErr**)
  
A estrutura bigdata que especifica os dados recuperados ou um erro é que os dados não podem ser recuperados ou o nome não está definido. Quando a função retorna, o membro **hData** do **XLOPER**/ **XLOPER12** contém um identificador para os dados nomeados.  _pxRes_ deve ser liberado em uma chamada para **xlFree** quando não for mais necessário. 
  
_pxName_ (**xltypeStr**)
  
Uma cadeia de caracteres especificando o nome dos dados.
  
## <a name="remarks"></a>Comentários

O Microsoft Excel é proprietário do identificador de memória retornado em **hData**. No Windows, a alça é um identificador de memória global (alocado pela função **GlobalAlloc** ). 
  
## <a name="see-also"></a>Confira também

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

