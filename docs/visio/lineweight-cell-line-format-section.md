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
ms.openlocfilehash: 654a93f939226bedab2e40ab591dad0e3f872267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412244"
---
# <a name="lineweight-cell-line-format-section"></a>Célula LineWeight (Seção Line Format)

Determina a espessura da linha de uma forma. Defina a espessura inserindo um número com uma unidade de medida válida.
  
## <a name="remarks"></a>Comentários

Você também pode definir o valor da célula LineWeight na caixa de diálogo **Linha** (na guia **Página Inicial**, no grupo **Forma**, clique em **Linha**, aponte para **Espessura** e clique em **Mais Linhas**).
  
Se a unidade de medida não for inserida, a unidade de medida do texto especificado  na caixa de diálogo Opções do **Visio** será usada (clique na guia Arquivo e em **Opções).** A espessura da linha não depende da escala do desenho. Se o desenho estiver dimensionado, a espessura será a mesma. 
  
Para fazer referência à célula IsDropSource pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LineWeight  <br/> |
   
Para fazer referência à célula LineWeight pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice de linha:  <br/> |**visRowLine** <br/> |
| Índice de célula:  <br/> |**visLineWeight** <br/> |
   

