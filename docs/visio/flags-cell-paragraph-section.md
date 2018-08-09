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
ms.openlocfilehash: b471d08556bedf68ce75595b9c211758297e8352
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771879"
---
# <a name="flags-cell-paragraph-section"></a>Célula Flags (Seção Paragraph)

Indica a direção do texto: da esquerda para a direita ou vice-versa.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |A direção do texto é da esquerda para a direita (o padrão).  <br/> |
|1  <br/> |A direção do texto é da direita para a esquerda.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor desta célula corresponde à configuração **direção** na guia **parágrafo** na caixa de diálogo **texto** (na guia **página inicial** , clique na seta **fonte** ), que aparecerá somente se o texto de um idioma que usa um complexo scripts ficou adicionada na caixa de diálogo **Preferências de idioma do Microsoft Office** . (Clique em **Iniciar**, clique em **Todos os programas**, clique em **Microsoft Office**, clique em **Ferramentas do Microsoft Office**e clique em **Preferências de idioma do Microsoft Office**.) 
  
Para obter uma referência para a célula Flags pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Para.Flags [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para a célula Flags pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionParagraph** <br/> |
|Índice da linha:  <br/> |**visRowParagraph** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visFlags** <br/> |
   

