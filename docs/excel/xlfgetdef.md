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
ms.openlocfilehash: 014db553156849d84bd07e0e416f8cb3fefb4e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421995"
---
# <a name="xlfgetdef"></a>xlfGetDef

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o nome, como texto, que é definido para uma determinada área, valor ou fórmula em uma área de trabalho. No Excel, esse valor é  exibido na coluna Nome da caixa de diálogo  Gerenciador de  Nomes, exibida quando você clica no Gerenciador de Nomes na seção Nomes Definidos da **guia Fórmulas.**  Use **xlfGetDef** para obter o nome que corresponde a uma definição. Para obter a definição de um nome, use [xlfGetName](xlfgetname.md).
  
```cpp
Excel12(xlfGetDef, LPXLOPER12 pxRes, 3, LPXLOPER12 pxDefText, LPXLOPER12 pxDocumentText, LPXLOPER12 pxTypeNum);
```

## <a name="parameters"></a>Parâmetros

_pxDefText_ (**xltypeStr**)
  
Pode ser qualquer coisa à qual você possa definir um nome, incluindo uma referência, um valor, um objeto ou uma fórmula.
  
As referências devem ser fornecidas no estilo R1C1, como  `"R3C5"` . Se _pxDefText_ for um valor ou uma fórmula, não será necessário  incluir o sinal de igual exibido na coluna Fazer Referência à, na caixa de diálogo **Gerenciador** de Nomes. Se houver mais de um nome para  _pxDefText_, **xlfGetDef** retornará o primeiro nome. Se nenhum nome corresponde  _a pxDefText_, **xlfGetDef** retorna o  `#NAME?` valor de erro. 
  
_pxDocumentText_ (**xltypeStr**)
  
Especifica a planilha em que  _pxDefText_ está. Se  _pxDocumentText_ for omitido, será assumido como sendo a planilha ativa. 
  
_pxTypeNum_ (**xltypeNum**)
  
Um número de 1 a 3 especificando quais tipos de nomes são retornados.
  
|**_pxTypeNum_**|**Retorna**|
|:-----|:-----|
|1 ou omitido  <br/> |Somente nomes normais.  <br/> |
|2   <br/> |Somente nomes ocultos.  <br/> |
|3   <br/> |Todos os nomes.  <br/> |
   
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 _pxRes_ (**xltypeStr** ou **xltypeErr**)
  
Retorna o nome associado à definição especificada.
  
## <a name="remarks"></a>Comentários

A tabela a seguir lista quatro exemplos dos valores retornados por uma chamada para **xlfGetDef** com os argumentos especificados. 
  
|**Nome definido no Excel**|**_pxDefText_**|**_pxDocumentText_**|**_pxTypeNum_**|**Valor retornado**|
|:-----|:-----|:-----|:-----|:-----|
|O intervalo especificado em Sheet4 é denominado Vendas.  <br/> |"R2C2:R9C6"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Vendas"  <br/> |
|O valor 100 em Sheet4 é definido como Constante.  <br/> |"100"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"Constante"  <br/> |
|A fórmula especificada em Sheet4 é denominada SumTotal.  <br/> |"SUM(R1C1:R10C1)"  <br/> |"Sheet4"  <br/> |\<omitido\>  <br/> |"SumTotal"  <br/> |
|3 é definido como o contador de nomes ocultos na planilha ativa.  <br/> |"3"  <br/> |\<omitido\>  <br/> |2   <br/> |"Contador"  <br/> |
   
## <a name="see-also"></a>Confira também

- [xlfGetName](xlfgetname.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

