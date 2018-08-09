---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- função xlSet [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765493"
---
# <a name="xlset"></a>xlSet

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Coloca valores de constantes em intervalos de células ou muito rapidamente. Para obter mais informações, consulte "xlSet e pastas de trabalho com fórmulas de matriz" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parâmetros

_pxReference_ (**xltypeRef** ou **xltypeSRef**)
  
Uma referência retangular descrevendo o destino de uma ou mais células. A referência deve descrever células adjacentes, portanto isso em um **xltypeRef** `val.mref.lpmref->count` deve ser definida como 1. 
  
_pxValue_
  
O valor ou valores sejam colocadas em uma ou mais células. Para obter mais informações, consulte a seção "Comentários".
  
## <a name="remarks"></a>Comentários

### <a name="pxvalue-argument"></a>argumento pxValue

_pxValue_ pode ser um valor ou uma matriz. Se for um valor, o intervalo de destino inteira é preenchido com esse valor. Se for uma matriz (**xltypeMulti**), os elementos da matriz são colocados nos locais correspondentes no retângulo.
  
Se você usar uma matriz horizontal para o segundo argumento, ele é duplicado para baixo para preencher todo o retângulo. Se você usar uma matriz vertical, ele é duplicado direita para preencher o retângulo inteiro. Se você usar uma matriz retangular e é muito pequeno para o intervalo retangular que você deseja colocá-lo no, aquele intervalo é preenchido com s **# N/d**.
  
Se o intervalo de destino for menor que a matriz de origem, os valores são copiados em até os limites do intervalo de destino e os dados extras serão ignorados.
  
Para limpar um elemento do retângulo de destino, use um elemento de matriz do tipo **xltypeNil** da matriz de origem. Para limpar o retângulo de destino inteira, omita o segundo argumento. 
  
### <a name="restrictions"></a>Restrições

**xlSet** não pode ser desfeita. Além disso, ele destrua qualquer informação de desfazer que pode ter sido disponível antes. 
  
**xlSet** pode colocar apenas constantes, não fórmulas em células. 
  
**xlSet** se comporta como uma função equivalente de comando de classe 3; ou seja, ele estará disponível somente dentro de uma DLL quando a DLL é chamada a partir de um objeto, macro, menu, barra de ferramentas, tecla de atalho ou no botão **Executar** na caixa de diálogo **Macro** (acessada a partir da guia **Exibir** da faixa de opções inicial no Excel 2007 e as ferramentas de ** **menu em versões anteriores). 
  
## <a name="example"></a>Exemplo

O exemplo a seguir preenche B205:B206 com o valor passado em de uma macro. Exemplo da função este comando requer um argumento e portanto funcionará somente se for chamado a partir de uma folha de macro XLM ou um módulo do VBA usando o método Application **Run** . 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>Confira também

- [xlCoerce](xlcoerce.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

