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
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772428"
---
# <a name="onpage-cell-print-properties-section"></a>Célula OnPage (Seção Print Properties)

Indica se o desenho é impresso em um número específico de páginas. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|VERDADEIRO  <br/> |Ajuste a página de desenho a um número definido de páginas impressas.  <br/> |
|FALSO  <br/> |Não ajusta a página de desenho a um número definido de páginas impressas (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Se a célula OnPage for definida como VERDADEIRO, o Microsoft Visio usa as células PagesX e PagesY para determinar o número de páginas impressas com o qual ajustará o desenho. Os valores das células ScaleX e ScaleY são ignorados. Essa pode ser considerada uma configuração de "escala automática".
  
Esse valor corresponde à opção **caber** na guia **Configurar impressão** , na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). 
  
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
   

