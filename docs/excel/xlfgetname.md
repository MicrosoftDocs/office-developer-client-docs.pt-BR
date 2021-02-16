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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436626"
---
# <a name="xlfgetname"></a>xlfGetName

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna a definição de um  nome como aparece  na coluna Refere-se à caixa de diálogo  Gerenciador de Nomes, exibida quando você clica em Gerenciador de Nomes na seção Nomes Definidos da guia **Fórmulas.**  Se a definição contiver referências, elas serão fornecidas como referências de estilo R1C1. Use **xlfGetName** para verificar o valor definido por um nome. Para obter o nome que corresponde a uma definição, use [xlfGetDef](xlfgetdef.md).
  
```cpp
Excel12(xlfGetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxInfoType);
```

## <a name="parameters"></a>Parâmetros

_pxNameText_ (**xltypeStr**)
  
Pode ser um nome definido na planilha; uma referência externa a um nome definido na lista de trabalho ativa, por exemplo; ou uma referência externa a um nome definido em uma determinada área de trabalho aberta, por  `"!Sales"` exemplo,  `"[Book1]SHEET1!Sales"` .  _pxNameText_ também pode ser um nome oculto. 
  
_pxInfoType_ (**xltypeBool**)
  
Especifica o tipo de informação a ser retornada sobre o nome. Se **FALSO** ou omitido, a definição será retornada. Se **TRUE**, retorna **TRUE** se o nome estiver definido apenas para a planilha, **FALSE** se o nome estiver definido para toda a pasta de trabalho. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

_pxRes_ (**xltypeStr**, **xltypeBool** ou **xltypeErr**)
  
Dependendo do valor passado para  _pxInfoType_, retorna a definição do nome especificado (**xltypeStr**) ou **TRUE** ou **FALSE** (**xltypeBool**).
  
## <a name="remarks"></a>Comentários

Se  a caixa de seleção Proteger planilha e conteúdo  de células bloqueadas tiver sido marcada na caixa de diálogo Proteger Planilha para proteger a pasta de trabalho que contém o nome, **xlfGetName** retornará o valor `#N/A` de erro. Para ver a **caixa de diálogo** Proteger Planilha, clique em Proteger **Planilha** na seção **Alterações** da **guia** Revisão. 
  
A tabela a seguir lista três exemplos dos valores retornados por uma chamada para **xlfGetDef** com o argumento  _pxNameText_ especificado. 
  
|**Definição no Excel**|**_pxNameText_**|**Valor retornado**|
|:-----|:-----|:-----|
|O nome Vendas em uma planilha é definido como o número 523.  <br/> |"Vendas"  <br/> |"=523"  <br/> |
|O nome Lucro na planilha ativa é definido como a fórmula =Sales-Costs.  <br/> |"! Lucro"  <br/> |"=Sales-Costs"  <br/> |
|O nome Banco de Dados na planilha ativa é definido como o intervalo A1:F500.  <br/> |"! Banco de dados"  <br/> |"=R1C1:R500C6"  <br/> |
   
## <a name="see-also"></a>Confira também

- [xlfGetDef](xlfgetdef.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

