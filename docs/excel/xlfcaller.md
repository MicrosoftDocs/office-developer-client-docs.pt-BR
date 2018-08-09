---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- função xlfCaller [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765461"
---
# <a name="xlfcaller"></a>xlfCaller

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna informações sobre a célula, o intervalo de células, o comando em um menu, a ferramenta em uma barra de ferramentas ou objeto que chamou o comando DLL ou a função que está sendo executado.
  
|**Chamado a partir de código**|**Retorna**|
|:-----|:-----|
|DLL  <br/> |A identificação do registro.  <br/> |
|Uma única célula  <br/> |Uma referência de célula única.  <br/> |
|Uma fórmula de matriz com várias células  <br/> |Uma referência de várias célula.  <br/> |
|Uma expressão de formatação condicional  <br/> |Uma referência à célula à qual a condição de formatação é aplicada.  <br/> |
|Um menu  <br/> | Uma matriz de linha única de quatro elementos:  <br/>  ID de barra.  <br/>  A posição do menu.  <br/>  A posição de submenu.  <br/>  A posição do comando.  <br/> |
|Uma barra de ferramentas  <br/> | Uma matriz de linha única de dois elementos:  <br/>  O número de barra de ferramentas para barras de ferramentas internas ou o nome da barra de ferramentas para barras de ferramentas personalizadas.  <br/>  A posição na barra de ferramentas.  <br/> |
|Um objeto graphic  <br/> |O identificador de objeto (nome de objeto).  <br/> |
|Um comando associado a um xlcOnEnter, em. Inserir, evento interceptação  <br/> |Uma referência para a célula ou células inseridas.  <br/> |
|Um comando associado a um xlcOnDoubleclick, em. DOUBLECLICK, evento desvio.  <br/> |A célula que foi clicado duas vezes (não necessariamente a célula ativa).  <br/> |
|Macro Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate  <br/> |O nome da folha de chamada.  <br/> |
|Outros métodos não listados  <br/> |#REF! Erro  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O valor de retorno é um dos seguintes **XLOPER**/ **XLOPER12** tipos de dados: **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**. Desde que três desses tipos de apontar para a memória alocada, o valor de retorno de **xlfCaller** deve sempre ser liberado em uma chamada para a [função xlFree](xlfree.md) quando ele não é mais necessária. 
  
Para obter mais informações sobre **XLOPERs**/ **XLOPER12s** consulte [Gerenciamento de memória no Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Comentários

Essa função é a função apenas não-planilha que pode ser chamada a partir de uma função de planilha DLL/XLL. Outras funções de informações XLM só podem ser chamadas de comandos ou equivalente de folha de macro funções.
  
## <a name="example"></a>Exemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Esta função chama uma macro de comando (xlcSelect) e funcionará corretamente somente quando chamadas de uma folha de macro.
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)

