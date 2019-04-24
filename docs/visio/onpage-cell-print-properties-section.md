---
title: Célula OnPage (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indica se o desenho é impresso em um número específico de páginas.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360981"
---
# <a name="onpage-cell-print-properties-section"></a>Célula OnPage (Seção Print Properties)

Indica se o desenho é impresso em um número específico de páginas. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|TRUE  <br/> |Ajustar a página de desenho a um número definido de páginas da impressora.  <br/> |
|FALSE  <br/> |Não ajusta a página de desenho a um número definido de páginas impressas (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Se a célula OnPage for definida como VERDADEIRO, o Microsoft Visio usa as células PagesX e PagesY para determinar o número de páginas impressas com o qual ajustará o desenho. Os valores das células ScaleX e ScaleY são ignorados. Essa pode ser considerada uma configuração de "escala automática".
  
Esse valor corresponde à opção **ajustar para** , na guia **Configurar impressão** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ). 
  
Para obter uma referência para a célula OnPage pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |OnPage  <br/> |
   
Para obter uma referência para a célula OnPage pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPrintProperties** <br/> |
|Índice da célula:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

