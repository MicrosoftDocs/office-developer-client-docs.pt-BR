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
ms.openlocfilehash: 63bfc6e94950a621c2367b2d35d25e3de48b344f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765463"
---
# <a name="xlfgetname"></a>xlfGetName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna a definição de um nome como ele aparece na coluna da caixa de diálogo **Gerenciador de nome** , que é exibida quando você clicar em **Nome do gerente** , na seção **Nomes definidos** na guia **fórmulas** **refere-se a** . Se a definição contém referências, ele recebe como referências em estilo L1C1. Use **xlfGetName** para verificar o valor definido por um nome. Para obter o nome que corresponde a uma definição, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parâmetros

_pxNameText_ (**xltypeStr**)
  
Pode ser um nome definido na planilha; uma referência externa para um nome definido na planilha ativa, por exemplo, `"!Sales"`; ou uma referência externa para um nome definido em uma determinada pasta de trabalho aberta, por exemplo, `"[Book1]SHEET1!Sales"`.  _pxNameText_ também pode ser um nome oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica o tipo de informações que serão retornadas sobre o nome. Se **Falso** ou omitido, a definição é retornada. Se **TRUE**, retorna **TRUE** se o nome está definido apenas da planilha, **FALSE** se o nome está definido para a pasta de trabalho inteira. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

_pxRes_ (**xltypeStr**, **xltypeBool**ou **xltypeErr**)
  
Dependendo do valor passado para _pxInfoType_, retorna a definição do nome especificado (**xltypeStr**) ou **TRUE** ou **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Comentários

Se a caixa de seleção de **proteger a planilha e o conteúdo de células bloqueadas** tiver sido selecionada na caixa de diálogo **Proteger planilha** para proteger a pasta de trabalho que contém o nome, **xlfGetName** retorna o `#N/A` o valor de erro. Para ver a caixa de diálogo **Proteger planilha** , clique em **Proteger planilha** na seção **alterações** da guia **revisão** . 
  
A tabela a seguir lista os três exemplos dos valores retornados por uma chamada para **xlfGetDef** com o argumento especificado _pxNameText_ . 
  
|**Definição no Excel**|**_pxNameText_**|**Valor retornado**|
|:-----|:-----|:-----|
|O nome de vendas em uma planilha é definido como o número 523.  <br/> |"Vendas"  <br/> |"= 523"  <br/> |
|O nome de lucro na planilha ativa é definido como a fórmula = custos de vendas.  <br/> |"! Lucro"  <br/> |"= Custos de vendas"  <br/> |
|O nome do banco de dados na planilha ativa é definido como o intervalo A1:F500.  <br/> |"! Banco de dados"  <br/> |"= R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Confira também

- [xlfGetDef](xlfgetdef.md)
- [Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)

