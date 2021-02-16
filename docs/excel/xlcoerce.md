---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- função xlcoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424830"
---
# <a name="xlcoerce"></a>xlCoerce

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Converte um tipo de **XLOPER** /  **XLOPER12 em** outro ou procura valores de célula em uma planilha. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parâmetros

 _pxSource_
  
O **XLOPER** /  **XLOPER12 de** origem que precisa ser convertido. 
  
 _pxDestType_ (**xltypeInt**)
  
(Opcional). Uma máscara de bits dos tipos resultantes que você está disposto a aceitar. Você deve usar o operador **OR** bit a bit ( | ) para especificar vários tipos possíveis. Se esse argumento for omitido, as referências a células individuais serão convertidas em um dos tipos de valor **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (se a célula referida estiver vazia) e referências a blocos de células serão convertidas em **xltypeMulti**. Isso torna **xlCoerce** a maneira mais conveniente de procurar valores de célula. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna o valor coerced (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** ou **xltypeMulti**).
  
## <a name="remarks"></a>Comentários

 **xlCoerce não** pode converter de ou **para xltypeBigData** ou **xltypeFlow**. Passar um **tipo xltypeMissing** ou **xltypeNil** como  _pxDestType_ é equivalente a omitir o argumento. A conversão pode falhar em alguns casos. Por exemplo, algumas cadeias de caracteres não podem ser convertidas em números, enquanto outras podem. 
  
Se uma matriz ou uma referência de várias células for convertida em um tipo de valor único, o resultado será o valor da célula ou do elemento de matriz superior esquerdo.
  
## <a name="example"></a>Exemplo

O código a seguir pode ser encontrado em  `\SAMPLES\EXAMPLE\EXAMPLE.C` . 
  
> [!NOTE]
> A **função xlcAlert** tenta converter implicitamente seu argumento em uma cadeia de caracteres para que a etapa de coerção mostrada aqui possa, na verdade, ser removida, e **xInt** possa ser passada diretamente para **xlcAlert**. Como **xlcAlert** é uma macro de comando, esse código só funciona corretamente quando chamado de uma folha de macro. 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>Confira também



[xlSet](xlset.md)


[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

