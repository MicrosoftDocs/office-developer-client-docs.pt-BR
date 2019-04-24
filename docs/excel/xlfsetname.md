---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- função xlfSetName [Excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6327ccf2cd18e42c3ef9abe538e6f669e498352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310273"
---
# <a name="xlfsetname"></a>xlfSetName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para criar e excluir nomes definidos associados à DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Parâmetros

_pxNameText_ (**xltypeStr**)
  
O nome do intervalo, que deve estar em conformidade com as limitações normais no Microsoft Excel em nomes válidos.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)
  
(Opcional). O valor, o conjunto de valores, a célula ou o intervalo de células que o _pxNameText_ está definido como. Se for omitido, o nome será excluído. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

_pxRes_ (**xltypeBool** ou **xltypeErr**)
  
TRUE se a operação foi bem-sucedida ou FALSE se o nome não pôde ser criado ou excluído. Retorna #VALUE! se um ou mais argumentos forem inválidos.
  
## <a name="remarks"></a>Comentários

Quando um comando ou função é registrado usando **xlfRegister** com um argumento _pxFunctionText_ válido, o Excel cria um nome associado ao recurso dll. Quando sua DLL estiver sendo descarregada, esses nomes devem ser excluídos usando a [função xlfSetName](xlfsetname.md). No enTanto, devido a um problema conhecido no Excel, essa operação de exclusão falha. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Exemplo

Consulte o código para a função **xlAutoClose** no `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

