---
title: Célula PaperKind (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60067
localization_priority: Normal
ms.assetid: b2c9616f-a144-eb99-54b6-b53745c7b4d6
description: Especifica o tipo de papel no qual a página será impressa.
ms.openlocfilehash: 694aa1fb8b52f5ae323c47e9aab8715b4a48dfb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408443"
---
# <a name="paperkind-cell-print-properties-section"></a>Célula PaperKind (Seção Print Properties)

Especifica o tipo de papel no qual a página será impressa.
  
## <a name="remarks"></a>Comentários

Essa configuração corresponde  à configuração  Tamanho do Papel na caixa de  diálogo Configurar Impressão (na guia **Design,** clique na seta Configurar Página e, na guia Configurar Impressão, clique no botão Configurar).   
  
Os valores numéricos nesta célula são mapeados para constantes (prefixadas com DMPAPER) definidas para seleções de papel no arquivo wingdi.h do Microsoft Windows. 
  
Para obter uma referência para a célula PaperKind pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PaperKind  <br/> |
   
Para obter uma referência para a célula PaperKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice de célula:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

