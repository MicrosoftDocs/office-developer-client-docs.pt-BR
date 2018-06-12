---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- função xlfSetName [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765464"
---
# <a name="xlfsetname"></a>xlfSetName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para criar e excluir nomes definidos associados a DLL.
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>Par�metros

_pxNameText_ (**xltypeStr**)
  
O nome do intervalo, que deve se adequar às limitações usuais no Microsoft Excel sobre nomes válidos.
  
_pxNameDefinition_ (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeMulti**, **xltypeSRef**, **xltypeRef**ou **xltypeInt**)
  
(Opcional). O valor, o conjunto de valores, célula ou intervalo de células que _pxNameText_ é definido como. Se for omitido, o nome é excluído. 
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

_pxRes_ (**xltypeBool** ou **xltypeErr**)
  
TRUE se a operação foi bem-sucedida ou FALSE se o nome não pôde ser criado ou excluído. Retorna #VALUE! Se um ou mais dos argumentos eram inválida.
  
## <a name="remarks"></a>Coment�rios

Quando um comando ou uma função é registrado usando **xlfRegister** com um argumento válido _pxFunctionText_ , o Excel criará um nome associado a DLL de recurso. Quando sua DLL está sendo descarregado, tais nomes devem ser excluídos usando a [função xlfSetName](xlfsetname.md). No entanto, devido a um problema conhecido no Excel, essa operação de exclusão falhar. Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
### <a name="example"></a>Example

Ver o código para a função **xlAutoClose** em `\SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [Funções de XLM API C essenciais e úteis](essential-and-useful-c-api-xlm-functions.md)

