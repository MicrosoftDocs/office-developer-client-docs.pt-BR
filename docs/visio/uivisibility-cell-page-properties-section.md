---
title: Célula UIVisibility (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60090
localization_priority: Normal
ms.assetid: df7f79df-770a-4868-e7e2-05c3828e23eb
description: Determina se o nome da página será exibido na interface do usuário.
ms.openlocfilehash: dcb4a14ff89c7f5c77916e6b188aaf87e1711ab0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773234"
---
# <a name="uivisibility-cell-page-properties-section"></a>Célula UIVisibility (Seção Page Properties)

Determina se o nome da página será exibido na interface do usuário.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Exibe o nome da página na interface do usuário (o padrão).  <br/> |**visUIVNormal** <br/> |
|1  <br/> |Não exibe o nome da página na interface do usuário.  <br/> |**visUIVHidden** <br/> |
   
## <a name="remarks"></a>Coment�rios

Definindo a célula UIVisibility como **visUIVHidden** impede que a página que aparecem em qualquer lugar na interface de usuário onde a cadeia de caracteres contendo o nome da página aparece. Por exemplo, a página não seria listada como uma opção no **Gerenciador de desenho** ou nas guias de página. A página permanece acessível, no entanto, se você usar caminhos de automação ou da interface do usuário que não inclua o nome da página, por exemplo, o comando **Imprimir** . 
  
 Esta célula é destinada para uso com páginas do documento; ele não é destinado para uso com páginas de sobreposição de marcação, que possuem a célula UIVisibility definida como **visUIVHidden** por padrão e não deve ser alterado. 
  
> [!NOTE]
> Para ocultar uma página do comando **Imprimir** do documento, torná-lo uma página de plano de fundo (a propriedade**Type** é **visTypeBackground** ) que não é usado como um plano de fundo por qualquer página (as formas em páginas são impressas quando uma página utilizá-lo como um plano de fundo é de plano de fundo impresso). Comando **Imprimir** do documento funciona somente com páginas indexadas e páginas de plano de fundo não estão indexadas. 
  
Para obter uma referência para a célula UIVisibility pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |UIVisibility  <br/> |
   
Para obter uma referência para a célula UIVisibility pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageUIVisibility** <br/> |
   

