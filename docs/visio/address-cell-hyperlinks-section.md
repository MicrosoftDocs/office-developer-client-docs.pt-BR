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
ms.openlocfilehash: 840ce0c4ce73da378f80e5d8a185073ac3915daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771272"
---
# <a name="address-cell-hyperlinks-section"></a>Célula Address (Seção Hyperlinks)

Especifica uma URL, um nome de arquivo ou um caminho UNC para o qual ir.
  
Você pode especificar o endereço como um caminho relativo com base no caminho de base definido para o documento na caixa de **base do hiperlink** na guia **Resumo** da caixa de diálogo **Propriedades** (clique na guia **arquivo** , clique em **Info*** * propriedades * * e clique em **Propriedades avançadas**). Se o documento não tiver nenhum caminho de base, o aplicativo navegará com base no caminho do documento. Se o documento não tiver sido salvo, o hiperlink é indefinido.
  
## <a name="remarks"></a>Comentários

Você pode também definir o valor da célula Address na caixa de diálogo **Hiperlinks** (clique em **Hiperlink** na guia **Inserir**). 
  
Para fazer referência à célula Address pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Hiperlink. *nome* . Endereços onde Hyperlink. *nome* é o nome da linha do hiperlink  <br/> |
   
Para fazer referência à célula Address pelo nome, a partir de outra fórmula ou de um programa, usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionHyperlink** <br/> |
| Índice da linha:  <br/> |**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visHLinkAddress** <br/> |
   

