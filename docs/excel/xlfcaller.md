---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- função xlfCaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405727"
---
# <a name="xlfcaller"></a>xlfCaller

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna informações sobre a célula, o intervalo de células, o comando em um menu, uma ferramenta em uma barra de ferramentas ou um objeto que chamou o comando DLL ou a função que está sendo executada no momento.
  
|**Código chamado de**|**Retorna**|
|:-----|:-----|
|DLL  <br/> |A ID de registro.  <br/> |
|Uma única célula  <br/> |Uma referência de célula única.  <br/> |
|Uma fórmula de matriz de várias células  <br/> |Uma referência de várias células.  <br/> |
|Uma expressão de formatação condicional  <br/> |Uma referência à célula à qual a condição de formatação é aplicada.  <br/> |
|Um menu  <br/> | Uma matriz de linha única de quatro elementos:  <br/>  A identificação da barra.  <br/>  A posição do menu.  <br/>  A posição do submenu.  <br/>  A posição do comando.  <br/> |
|Uma barra de ferramentas  <br/> | Uma matriz de linha única de dois elementos:  <br/>  O número da barra de ferramentas para barras de ferramentas internas ou o nome da barra de ferramentas para barras de ferramentas personalizadas.  <br/>  A posição na barra de ferramentas.  <br/> |
|Um objeto gráfico  <br/> |O identificador de objeto (nome do objeto).  <br/> |
|Um comando associado a um xlcOnEnter, em. INSERIR, interceptação de eventos  <br/> |Uma referência à célula ou células inseridas.  <br/> |
|Um comando associado a um xlcOnDoubleclick, em. DOUBLECLICK, interceptação de eventos.  <br/> |A célula que foi clicada duas vezes (não necessariamente a célula ativa).  <br/> |
|Macro Auto_Open, AutoClose, Auto_Activate ou Auto_Deactivate  <br/> |O nome da folha de chamada.  <br/> |
|Outros métodos não listados  <br/> |#REF! Erro  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O valor de retorno é um dos seguintes tipos de dados **XLOPER**/ **XLOPER12** : **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**ou **xltypeMulti**. Como três desses tipos apontam para a memória alocada, o valor de retorno de **xlfCaller** deve sempre ser liberado em uma chamada para a [função xlFree](xlfree.md) quando ele não for mais necessário. 
  
Para obter mais informações sobre **XLOPERs**/ **XLOPER12s** , consulte [Gerenciamento de memória no Excel](memory-management-in-excel.md).
  
## <a name="remarks"></a>Comentários

Essa função é a única função que não é de planilha que pode ser chamada de uma função de planilha DLL/XLL. Outras funções de informações de XLM só podem ser chamadas de comandos ou funções equivalentes de planilha de macro.
  
## <a name="example"></a>Exemplo

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Essa função chama uma macro de comando (xlcSelect) e funcionará corretamente somente quando for chamado a partir de uma folha de macro.
  
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



[Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

