---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- função funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765378"
---
# <a name="funcsum"></a>FuncSum

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de planilha definida pelo usuário de exemplo que leva argumentos de 1 a 29 e computa sua soma. Cada argumento pode ser um único número, um intervalo ou uma matriz. Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parâmetros

 _px1-px29_ (**LPXLOPER12**)
  
Ponteiros para os argumentos **XLOPER12** . A função aceita qualquer tipo de tipo de entrada, mas é codificada somente para operar em números, literais matrizes de números e intervalos que contenham somente números ou células em branco. Se menos de 29 argumentos é fornecido, os argumentos restantes são fornecidos como **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

(**XltypeNum LPXLOPER12** ou **xltypeErr**)
  
A soma dos argumentos ou #VALUE! Se houver não-numéricos na lista de argumentos fornecidos ou em uma célula em um intervalo ou de um elemento em uma matriz.
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

