---
title: Célula TxtPinX (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina o x-coordenadas do centro do bloco de texto de rotação em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773193"
---
# <a name="txtpinx-cell-text-transform-section"></a>Célula TxtPinX (Seção Text Transform)

Determina o *x* -coordenadas do centro do bloco de texto de rotação em relação à origem da forma. A fórmula padrão é: 
  
= A largura \* 0.5
  
## <a name="remarks"></a>Coment�rios

Para obter uma referência à célula TxtPinX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | TxtPinX  <br/> |
   
Para obter uma referência à célula TxtPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowTextXForm** <br/> |
| Índice da célula:  <br/> |**visXFormPinX** <br/> |
   

