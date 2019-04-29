---
title: Célula PlowCode (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420350"
---
# <a name="plowcode-cell-page-layout-section"></a>Célula PlowCode (Seção Page Layout)

Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|,0  <br/> |Não mover as formas  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Mover as formas  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **layout e roteamento** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ) usando a caixa de seleção **afastar outras formas ao soltar** . 
  
Para obter uma referência para a célula PlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PlowCode  <br/> |
   
Para obter uma referência para a célula PlowCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOPlowCode** <br/> |
   

