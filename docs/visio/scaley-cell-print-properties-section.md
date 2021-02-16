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
description: Especifica a porcentagem de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406987"
---
# <a name="scaley-cell-print-properties-section"></a>Célula ScaleY (Seção Print Properties)

Especifica a porcentagem de ampliação da página de desenho na página impressa.
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando a célula OnPage está definida como FALSO. As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor  da configuração Ajustar para na guia  Configurar Impressão da caixa de diálogo Configurar Página (na guia **Design,** clique na seta Configurar Página).   
  
Para obter uma referência para a célula ScaleY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ScaleY  <br/> |
   
Para obter uma referência para a célula ScaleY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice de célula:  <br/> |**visPrintPropertiesScaleY** <br/> |
   

