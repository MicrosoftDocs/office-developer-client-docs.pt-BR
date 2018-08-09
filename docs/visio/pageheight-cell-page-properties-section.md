---
title: Célula PageHeight (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contém a altura da página impressa em unidades de desenho.
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772447"
---
# <a name="pageheight-cell-page-properties-section"></a>Célula PageHeight (Seção Page Properties)

Contém a altura da página impressa em unidades de desenho.
  
## <a name="remarks"></a>Comentários

Também é possível definir a altura da página na guia **Tamanho da Página** da caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página**) ou redimensionar manualmente a página com o mouse. 
  
Para obter uma referência para a célula PageHeight pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |PageHeight  <br/> |
   
Para obter uma referência para a célula PageHeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPage** <br/> |
|Índice da célula:  <br/> |**visPageHeight** <br/> |
   

