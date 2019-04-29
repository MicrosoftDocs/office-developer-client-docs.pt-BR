---
title: Célula Flags (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033782
localization_priority: Normal
ms.assetid: 898bf89d-d00f-9769-a89d-787ef708eca5
description: 'Indica a direção do texto: da esquerda para a direita ou vice-versa.'
ms.openlocfilehash: af1e79b13d3d8bab2e7271eb79e68cf931871806
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413112"
---
# <a name="flags-cell-paragraph-section"></a>Célula Flags (Seção Paragraph)

Indica a direção do texto: da esquerda para a direita ou vice-versa.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|,0  <br/> |A direção do texto é da esquerda para a direita (o padrão).  <br/> |
|1  <br/> |A direção do texto é da direita para a esquerda.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor desta célula corresponde à configuração de **direção** da guia **parágrafo** da caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ), que aparece somente se um idioma que usa o texto de scripts complexos tiver sido adicionado na caixa de diálogo **preferências de idioma do Microsoft Office** . (Clique em **Iniciar**, **todos os programas**, **Microsoft Office**, **Ferramentas do Microsoft Office**e, em seguida, em preferências de **idioma do Microsoft Office**.) 
  
Para obter uma referência para a célula Flags pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Para. Flags [ *i* ] onde *i* = <1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Flags pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionParagraph** <br/> |
|Índice de linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visFlags** <br/> |
   

