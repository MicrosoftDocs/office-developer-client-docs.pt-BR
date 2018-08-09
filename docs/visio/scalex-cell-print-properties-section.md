---
title: Célula ScaleX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Especifica o percentual de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 1713e88f06dc93a2806e64cae3d7af20c9df1fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772843"
---
# <a name="scalex-cell-print-properties-section"></a>Célula ScaleX (Seção Print Properties)

Especifica o percentual de ampliação da página de desenho na página impressa.
  
## <a name="remarks"></a>Comentários

Esse valor é usado somente quando o valor da célula OnPage for FALSE. As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor na configuração **Ajustar** da guia **Configurar impressão** , na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). 
  
Para obter uma referência para a célula ScaleX pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ScaleX  <br/> |
   
Para obter uma referência para a célula ScaleX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesScaleX** <br/> |
   

