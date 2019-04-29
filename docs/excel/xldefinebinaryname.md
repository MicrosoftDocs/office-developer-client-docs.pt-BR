---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- função xlDefineBinaryName [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430249"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para alocar armazenamento persistente para um **xltypeBigData** **XLOPER**/ **XLOPER12**. Os dados com um nome binário definido são salvos com a pasta de trabalho e podem ser acessados pelo nome a qualquer momento. Para saber mais, confira "limitação de escopo de nome binário" em [problemas conhecidos no desenvolvimento XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parâmetros

 _pxName_ (**xltypeStr**)
  
Uma cadeia de caracteres especificando o nome dos dados. A cadeia de caracteres está sujeita às mesmas restrições de nomenclatura que os nomes definidos.
  
 _pxData_ (**xltypeBigData**)
  
Estrutura bigdata que especifica os dados a serem armazenados. Ao chamar essa função, o membro **lpbData** da estrutura **bigdata** deve apontar para os dados para os quais o nome está sendo definido, e o membro **cbData** deve conter o tamanho dos dados em bytes. 
  
Se o argumento _pxData_ não for especificado (**xltypeMissing**), a alocação nomeada especificada por _pxName_ será excluída. 
  
## <a name="see-also"></a>Confira também



[xlGetBinaryName](xlgetbinaryname.md)


[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problemas conhecidos no desenvolvimento do Excel XLL ](known-issues-in-excel-xll-development.md)

