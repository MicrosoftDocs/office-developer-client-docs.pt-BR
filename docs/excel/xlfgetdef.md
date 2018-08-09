---
title: xlfGetDef
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetdef
localization_priority: Normal
ms.assetid: 68f5edbd-9040-46d3-acd5-dd51ca82f6fa
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030c4e501e8a9eb4b6ce29d7fe0e171324b50b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765484"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o nome, como texto, que é definido para uma determinada área, valor ou fórmula em uma pasta de trabalho. No Excel, esse valor é exibido na coluna **nome** da caixa de diálogo **Gerenciador de nome** , que é exibida quando você clicar em **Nome do gerente** na seção **Nomes definidos** , na guia **fórmulas** de uso **xlfGetDef** para obter o nome que corresponde a uma definição. Para obter a definição de um nome, use [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parâmetros

_pxDefText_ (**xltypeStr**)
  
Pode ser a qualquer coisa que você pode definir um nome para se referir a, incluindo uma referência, um valor, um objeto ou uma fórmula.
  
Referências devem ser fornecidas em estilo L1C1, tais como `"R3C5"`. Se _pxDefText_ for um valor ou fórmula, não é necessário incluir o sinal de igualdade que é exibido na coluna **Refere-se a** na caixa de diálogo **Gerenciador de nome** . Se houver mais de um nome para _pxDefText_, **xlfGetDef** retorna o primeiro nome. Se nenhum nome corresponde _pxDefText_, **xlfGetDef** retorna o `#NAME?` o valor de erro. 
  
_pxDocumentText_ (**xltypeStr**)
  
Especifica a planilha que _pxDefText_ está em. Se _pxDocumentText_ for omitido, presume-se para ser da planilha ativa. 
  
_pxTypeNum_ (**xltypeNum**)
  
Um número de 1 a 3 para especificar quais tipos de nomes são retornados.
  
|**_pxTypeNum_**|**Retorna**|
|:-----|:-----|
|1 ou omitido  <br/> |Apenas nomes normais.  <br/> |
|2  <br/> |Apenas nomes ocultos.  <br/> |
|3  <br/> |Todos os nomes.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Retorna o nome associado à definição especificada.
  
## <a name="remarks"></a>Comentários

A tabela a seguir lista os quatro exemplos dos valores retornados por uma chamada para **xlfGetDef** com os argumentos especificados. 
  
|**Nome definido no Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valor retornado**|
|:-----|:-----|:-----|:-----|:-----|
|O intervalo especificado em Sheet4 é chamado Sales.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Vendas"  <br/> |
|O valor de 100 em Sheet4 é definido como constante.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Constante"  <br/> |
|A fórmula especificada no Sheet4 é nomeada SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"SumTotal"  <br/> |
|3 é definido como o contador de nome oculto na planilha ativa.  <br/> |"3"  <br/> |\<omitido\>  <br/> |2  <br/> |"Contador"  <br/> |
   
## <a name="see-also"></a>Confira também

- [xlfGetName](xlfgetname.md)
- [Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)

