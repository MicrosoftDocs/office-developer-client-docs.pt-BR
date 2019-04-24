---
title: xlfGetName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
keywords:
- xlfgetname
localization_priority: Normal
ms.assetid: 65780435-aaa2-47af-b44f-07be7aa769ee
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fdee0146ae2199097828e98abb96ffe43a64fc80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303882"
---
# <a name="xlfgetname"></a>xlfGetName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna a definição de um nome como ele aparece na coluna **refere-se a** da caixa de diálogo **Gerenciador de nomes** , que é exibida quando você clica em **Gerenciador de nomes** na seção **nomes definidos** da guia **fórmulas** . Se a definição contiver referências, elas serão dadas como referências em estilo L1C1. Use **xlfGetName** para verificar o valor definido por um nome. Para obter o nome que corresponde a uma definição, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parâmetros

_pxNameText_ (**xltypeStr**)
  
Pode ser um nome definido na planilha; uma referência externa a um nome definido na pasta de trabalho ativa, por exemplo `"!Sales"`,; ou uma referência externa para um nome definido em uma determinada pasta de trabalho aberta, por `"[Book1]SHEET1!Sales"`exemplo,.  _pxNameText_ também pode ser um nome oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica o tipo de informação a ser retornada sobre o nome. Se **false** ou omitido, a definição será retornada. Se **true**, retornará **true** se o nome for definido para apenas a planilha, **false** se o nome for definido para a pasta de trabalho inteira. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)
  
Dependendo do valor passado por _pxInfoType_, retorna a definição do nome especificado (**XltypeStr**) ou **true** ou **false** (**xltypeBool**).
  
## <a name="remarks"></a>Comentários

Se a caixa de seleção **proteger planilha e conteúdo de células bloqueadas** tiver sido selecionada na caixa de diálogo **proteger planilha** para proteger a pasta de trabalho que contém o `#N/A` nome, **xlfGetName** retornará o valor de erro. Para ver a caixa de diálogo **proteger planilha** , clique em **proteger planilha** na seção **alterações** da guia **revisão** . 
  
A tabela a seguir lista três exemplos de valores retornados por uma chamada a **xlfGetDef** com o argumento _pxNameText_ especificado. 
  
|**Definição no Excel**|**_pxNameText_**|**Valor retornado**|
|:-----|:-----|:-----|
|O nome vendas em uma planilha é definido como o número 523.  <br/> |Vendas  <br/> |"= 523"  <br/> |
|O nome de lucro na planilha ativa é definido como a fórmula = vendas-custos.  <br/> |"! Lucrativa  <br/> |"= Vendas-custos"  <br/> |
|O banco de dados de nomes na planilha ativa é definido como o intervalo a1: F500.  <br/> |"! AdventureWorks  <br/> |"= L1C1: R500C6"  <br/> |
   
## <a name="see-also"></a>Confira também

- [xlfGetDef](xlfgetdef.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

