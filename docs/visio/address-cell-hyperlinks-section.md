---
title: Célula Address (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338546"
---
# <a name="address-cell-hyperlinks-section"></a>Célula Address (Seção Hyperlinks)

Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.
  
Você pode especificar o endereço como um caminho relativo com base no caminho base definido para o documento na **caixa base do hiperlink** na guia **Resumo** da caixa de diálogo **Propriedades** (clique na guia **arquivo** , em **informações**, em * * Propriedades * * e, em seguida, clique em **Propriedades avançadas**. Se o documento não contiver um caminho de base, o aplicativo navegará com base no caminho do documento. Se o documento não tiver sido salvo, o hiperlink não será definido.
  
## <a name="remarks"></a>Comentários

Você pode também definir o valor da célula Address na caixa de diálogo **Hiperlinks** (clique em **Hiperlink** na guia **Inserir**). 
  
Para fazer referência à célula Address pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *nome* . Endereço onde hiperlink. *Name* é o nome da linha de hiperlink  <br/> |
   
Para fazer referência à célula address pelo nome, a partir de outra fórmula ou programa, usando a propriedade Cells **** , utilize: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHiperlink** <br/> |
| Índice de linha:  <br/> |**visRow1stHyperlink** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visHLinkAddress** <br/> |
   

