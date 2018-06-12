---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- função xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765468"
---
# <a name="xlcoerce"></a>xlCoerce

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Converte um tipo de **XLOPER**/ **XLOPER12** para outro ou aparências os valores de célula em uma planilha. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Par�metros

 _pxSource_
  
A fonte **XLOPER**/ **XLOPER12** que precisa ser convertido. 
  
 _pxDestType_ (**xltypeInt**)
  
(Opcional). Uma máscara de bits dos tipos resultantes você está disposto a aceitar. Você deve usar o operador **OR** bit a bit (|) para especificar vários tipos possíveis. Se esse argumento for omitido, o referências a células única são convertidas em um dos tipos de valor **xltypeStr** **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (se a célula referida estiver vazia) e referências aos blocos de células são convertidos **xltypeMulti**. Isso torna **xlCoerce** a maneira mais conveniente para consultar os valores de célula. 
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna o valor forçado (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**ou **xltypeMulti**).
  
## <a name="remarks"></a>Coment�rios

 **xlCoerce** não pode converter ou para **xltypeBigData** ou **xltypeFlow**. Passando um tipo **xltypeMissing** ou **xltypeNil** como _pxDestType_ é equivalente a omitir o argumento. Conversão pode falhar em alguns casos. Por exemplo, algumas cadeias de caracteres não podem ser convertidas em números, enquanto outros usuários possam. 
  
Se uma matriz ou uma referência de célula múltiplos é convertida em um tipo de valor único, o resultado é o valor do elemento superior e esquerdo de célula ou matriz.
  
## <a name="example"></a>Example

O código a seguir pode ser encontrado no `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> A função **xlcAlert** implicitamente tenta converter seu argumento em uma cadeia de caracteres, para que a etapa de coerção mostrada aqui na verdade pode ser removida e **xInt** poderia ser passadas diretamente para **xlcAlert**. Como **xlcAlert** uma macro de comando, este código só funciona corretamente quando chamado a partir de uma folha de macro. 
  
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


[Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

