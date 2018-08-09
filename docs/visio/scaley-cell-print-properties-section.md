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
description: Especifica o percentual de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772839"
---
# <a name="scaley-cell-print-properties-section"></a>Célula ScaleY (Seção Print Properties)

Especifica o percentual de ampliação da página de desenho na página impressa.
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando o valor da célula OnPage for FALSE. As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor na configuração **Ajustar** da guia **Configurar impressão** , na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). 
  
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
   

