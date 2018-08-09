---
title: Célula Description (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: Representa uma cadeia de caracteres de texto descritivo para um hiperlink.
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771728"
---
# <a name="description-cell-hyperlinks-section"></a>Célula Description (Seção Hyperlinks)

Representa uma cadeia de caracteres de texto descritivo para um hiperlink. 
  
## <a name="remarks"></a>Comentários

Utilize esta célula para armazenar comentários sobre o hiperlink; por exemplo, "Link para nosso site de preços na Web".
  
Você pode também definir o valor dessa célula na caixa de diálogo **Hiperlinks** (clique em **Hiperlinks** na guia **Inserir**). 
  
Para fazer referência à célula Description pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *Nome* . Descrição onde Hyperlink.  *Nome* é o nome da linha do hiperlink  <br/> |
   
Para fazer referência à célula Description pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkDescription** <br/> |
   

