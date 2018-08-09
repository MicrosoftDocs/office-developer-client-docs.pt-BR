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
ms.openlocfilehash: 03659553ab32afd20d1a5a40b85a8bbf107dbb08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772466"
---
# <a name="paperkind-cell-print-properties-section"></a>Célula PaperKind (Seção Print Properties)

Especifica o tipo de papel no qual a página será impressa.
  
## <a name="remarks"></a>Comentários

Essa configuração corresponde à configuração de **Tamanho do papel** na caixa de diálogo **Configurar impressão** (na guia **Design** , clique na seta **Configurar página** e, em seguida, na guia **Configurar impressão** , clique no botão **Configurar** ). 
  
Os valores numéricos dessa célula são mapeados de acordo com constantes (prefixadas com DMPAPER) definidas para seleções de papel no arquivo wingdi Microsoft Windows. 
  
Para obter uma referência para a célula PaperKind pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PaperKind  <br/> |
   
Para obter uma referência para a célula PaperKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesPaperKind** <br/> |
   

