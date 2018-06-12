---
title: Célula Transparency (Seção Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Determina o nível de transparência para uma camada de cor.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773168"
---
# <a name="transparency-cell-image-properties-section"></a>Célula Transparency (Seção Image Properties)

Determina o nível de transparência para uma camada de cor.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0 - 100  <br/> |Representa a porcentagem de transparência. O padrão é 0% (completamente opaco).  <br/> |
   
## <a name="remarks"></a>Comentários

Valores são arredondados para o meio por cento mais próximo. Um valor de 100% é completamente transparente. Embora uma camada com cor completamente transparente tenha a mesma na página de desenho como uma camada sem cor, ele se interage com outros objetos na página da mesma forma como se a transparência fosse 0%. Você também pode definir esse valor usando o controle deslizante na caixa de diálogo **Propriedades da camada** (na guia **página inicial** , no grupo **edição** , clique em **camadas**e, em seguida, clique em **Propriedades da camada**).
  
Para obter uma referência para a célula Transparency pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Transparency  <br/> |
   
Para obter uma referência para a célula Transparency pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowImage** <br/> |
|Índice da célula:  <br/> |**visImageTransparency** <br/> |
   

