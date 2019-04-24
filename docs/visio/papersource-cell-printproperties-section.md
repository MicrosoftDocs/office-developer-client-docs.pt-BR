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
ms.openlocfilehash: eb6e7daccb1743c43a30b34598e47187496e4aac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301460"
---
# <a name="papersource-cell-printproperties-section"></a>Célula PaperSource (Seção PrintProperties)

Determina a fonte de papel para a página. 
  
## <a name="remarks"></a>Comentários

Essa configuração corresponde à configuração **Fonte de Papel** da caixa de diálogo **Configurar Impressão** (na guia **Design**, clique na seta **Configurar Página** e, na guia **Configurar Impressão**, clique em **Configurar**).
  
Os valores numéricos nesta célula mapeiam as constantes (prefixadas com DMBIN) definidas para seleções de bin no arquivo WinGDI. h do Microsoft Windows; por exemplo, o valor 7 representa DMBIN_AUTO. 
  
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
   

