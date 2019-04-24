---
title: Célula ScaleY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Especifica a porcentagem de ampliação da página de desenho na página da impressora.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342725"
---
# <a name="scaley-cell-print-properties-section"></a>Célula ScaleY (Seção Print Properties)

Especifica a porcentagem de ampliação da página de desenho na página da impressora.
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando a célula OnPage está definida como FALSO. As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor da configuração **ajustar para** , na guia **Configurar impressão** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ). 
  
Para obter uma referência para a célula ScaleY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ScaleY  <br/> |
   
Para obter uma referência para a célula ScaleY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

