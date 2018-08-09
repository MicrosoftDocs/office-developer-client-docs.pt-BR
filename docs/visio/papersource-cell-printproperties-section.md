---
title: Célula PaperSource (Seção PrintProperties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60068
localization_priority: Normal
ms.assetid: 771a2ab4-578d-51c3-fabd-138f7952bb11
description: Determina a fonte de papel para a página.
ms.openlocfilehash: f1dedf210dfe0dd8cac3d36fdec03fb497f6572c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772462"
---
# <a name="papersource-cell-printproperties-section"></a>Célula PaperSource (Seção Print Properties)

Determina a fonte de papel para a página. 
  
## <a name="remarks"></a>Comentários

Essa configuração corresponde à configuração **Fonte de Papel** da caixa de diálogo **Configurar Impressão** (na guia **Design**, clique na seta **Configurar Página** e, na guia **Configurar Impressão**, clique em **Configurar**).
  
Os valores numéricos dessa célula são mapeados de acordo com constantes (prefixadas com DMBIN) definidos para seleções de compartimento no arquivo wingdi do Microsoft Windows; Por exemplo, o valor 7 representa DMBIN_AUTO. 
  
Para obter uma referência para a célula PaperSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PaperSource  <br/> |
   
Para obter uma referência para a célula PaperSource pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesPaperSource** <br/> |
   

