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
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427077"
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
|Índice de linha:  <br/> |**visRowPage** <br/> |
|Índice de célula:  <br/> |**visPageHeight** <br/> |
   

