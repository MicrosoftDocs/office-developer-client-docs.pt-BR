---
title: Célula LineWeight (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm585
localization_priority: Normal
ms.assetid: 16b0e293-eeef-34b4-aeb0-4472815dd543
description: Determina a espessura da linha de uma forma. Defina a espessura inserindo um número com uma unidade de medida válida.
ms.openlocfilehash: a5207607d90ef6a79dcb3acc191521b73e2cdf54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772208"
---
# <a name="lineweight-cell-line-format-section"></a>Célula LineWeight (Seção Line Format)

Determina a espessura da linha de uma forma. Defina a espessura inserindo um número com uma unidade de medida válida.
  
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula LineWeight na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**).
  
Se a unidade de medida não for inserida, a unidade de medida de texto especificado na caixa de diálogo **Opções do Visio** é usada (clique na guia **arquivo** e, em seguida, clique em **Opções**). Espessura da linha é independente da escala do desenho. Se o desenho estiver em escala, a espessura da linha permanece o mesmo. 
  
Para fazer referência à célula IsDropSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineWeight  <br/> |
   
Para fazer referência à célula LineWeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowLine** <br/> |
| Índice da célula:  <br/> |**visLineWeight** <br/> |
   

