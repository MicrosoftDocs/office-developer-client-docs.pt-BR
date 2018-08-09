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
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772519"
---
# <a name="plowcode-cell-page-layout-section"></a>Célula PlowCode (Seção Page Layout)

Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Não mover as formas  <br/> |**visPLOPlowNone** <br/> |
|1  <br/> |Mover as formas  <br/> |**visPLOPlowAll** <br/> |
   
## <a name="remarks"></a>Comentários

Você também pode definir o valor dessa célula na guia **Layout e roteamento** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ), usando a caixa de seleção **Afastar outras formas ao soltar** . 
  
Para obter uma referência para a célula PlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PlowCode  <br/> |
   
Para obter uma referência para a célula PlowCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOPlowCode** <br/> |
   

