---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- função xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765454"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para alocar armazenamento persistente para um **xltypeBigData** **XLOPER**/ **XLOPER12**. Dados com um nome definido de binário é salvo com a pasta de trabalho e podem ser acessados pelo nome, a qualquer momento. Para obter mais informações, consulte "Binário nome escopo limitação" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parâmetros

 _pxName_ (**xltypeStr**)
  
Uma cadeia de caracteres especificando o nome dos dados. A cadeia de caracteres está sujeito a mesma nomes definidos como restrições de nomeação.
  
 _pxData_ (**xltypeBigData**)
  
Estrutura de Bigdata especificando os dados a serem armazenados. Quando você chamar essa função, o membro **lpbData** da estrutura **bigdata** deve apontar para os dados para o qual o nome está definido e o membro **cbData diferente** deve conter o tamanho dos dados em bytes. 
  
Se o argumento _pxData_ não for especificado (**xltypeMissing**), a alocação nomeada especificada por _pxName_ é excluída. 
  
## <a name="see-also"></a>Confira também



[xlGetBinaryName](xlgetbinaryname.md)


[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md)

