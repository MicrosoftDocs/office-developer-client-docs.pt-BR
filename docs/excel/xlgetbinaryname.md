---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- função xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765470"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para retornar uma alça de dados salvos pela [função xlDefineBinaryName](xldefinebinaryname.md). Dados com um nome definido de binário é salvo com a pasta de trabalho e podem ser acessados pelo nome, a qualquer momento. Para obter mais informações, consulte "Binário" nomeie a limitação de escopo em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Par�metros

_pxRes_ (**xltypeBigData** ou **xltypeErr**)
  
Estrutura de Bigdata especificando que um erro ou os dados recuperados é os dados não pôde ser recuperada ou o nome não está definido. Quando a função retorna, o membro de **hdata** da **XLOPER**/ **XLOPER12** contém uma alça para os dados nomeadas.  _pxRes_ deve ser liberada em uma chamada para **xlFree** quando não são mais necessários. 
  
_pxName_ (**xltypeStr**)
  
Uma cadeia de caracteres especificando o nome dos dados.
  
## <a name="remarks"></a>Coment�rios

O Microsoft Excel possui o identificador de memória retornado em **hdata**. No Windows, o identificador é uma alça de memória global (alocada pela função **GlobalAlloc** ). 
  
## <a name="see-also"></a>Confira também

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

