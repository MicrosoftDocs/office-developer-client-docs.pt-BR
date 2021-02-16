---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- função xlset [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404600"
---
# <a name="xlset"></a>xlSet

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Coloca valores constantes em células ou intervalos muito rapidamente. For more information, see "xlSet and Workbooks with Array Formulas" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parâmetros

_pxReference_ (**xltypeRef** ou **xltypeSRef**)
  
Uma referência retangular que descreve a célula ou células de destino. A referência deve descrever células adjacentes, para que em **um xltypeRef** `val.mref.lpmref->count` seja definido como 1. 
  
_pxValue_
  
O valor ou valores a serem colocados na célula ou células. Para obter mais informações, consulte a seção "Comentários".
  
## <a name="remarks"></a>Comentários

### <a name="pxvalue-argument"></a>Argumento pxValue

_pxValue_ pode ser um valor ou uma matriz. Se for um valor, todo o intervalo de destino será preenchido com esse valor. Se for uma matriz (**xltypeMulti**), os elementos da matriz serão colocados nos locais correspondentes no retângulo.
  
Se você usar uma matriz horizontal para o segundo argumento, ela será duplicada para baixo para preencher todo o retângulo. Se você usar uma matriz vertical, ela será duplicada à direita para preencher todo o retângulo. Se você usar uma matriz retangular e ela for muito pequena para o intervalo retangular em que você deseja colocá-la, esse intervalo será **#N/A** s.
  
Se o intervalo de destino for menor que a matriz de origem, os valores serão copiados até os limites do intervalo de destino e os dados extras serão ignorados.
  
Para limpar um elemento do retângulo de destino, use um elemento de matriz do tipo **xltypeNil** na matriz de origem. Para limpar todo o retângulo de destino, omita o segundo argumento. 
  
### <a name="restrictions"></a>Restrições

**xlSet** não pode ser desfeita. Além disso, ele destrói todas as informações de desfazer que possam ter sido disponibilizadas antes. 
  
**xlSet** pode colocar somente constantes, não fórmulas, nas células. 
  
**xlSet** se comporta como uma função equivalente a comando de Classe 3; ou seja, ela só estará disponível dentro de uma DLL quando a DLL for chamada de  um objeto, macro, menu, barra de ferramentas, tecla de atalho ou o botão Executar na caixa de diálogo **Macro** (acessada na guia Exibir na faixa de opções a partir do Excel 2007 e do **menu** Ferramentas em versões anteriores).  
  
## <a name="example"></a>Exemplo

O exemplo a seguir preenche B205:B206 com o valor passado de uma macro. Este exemplo de função de comando requer um argumento e, portanto, só funcionará se for chamado de uma folha de macro XLM ou de um módulo VBA usando o **método Application.Run.** 
  
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

