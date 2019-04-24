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
description: Representa uma cadeia de texto descritiva de um hiperlink.
ms.openlocfilehash: b58e6dc3ec2fc3b64db00e0f19e0718fe897aaa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360239"
---
# <a name="description-cell-hyperlinks-section"></a>Célula Description (Seção Hyperlinks)

Representa uma cadeia de texto descritiva de um hiperlink. 
  
## <a name="remarks"></a>Comentários

Utilize esta célula para armazenar comentários sobre o hiperlink; por exemplo, "Link para nosso site de preços".
  
Você também pode definir o valor dessa célula na caixa de diálogo **Hiperlinks** (clique em **Hiperlink** na guia **Inserir**). 
  
Para obter uma referência à célula Descrição pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Hiperlink.  *Name*. Descrição em que Hiperlink.  *Name* é o nome da linha de hiperlink  <br/> |
   
Para obter uma referência à célula Description pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
| Índice de linha:  <br/> |**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visHLinkDescription** <br/> |
   

