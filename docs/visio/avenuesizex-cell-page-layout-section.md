---
title: Célula AvenueSizeX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Novo Layout de página e, em seguida, clique em mais opções de Layout).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771298"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Célula AvenueSizeX (Seção Page Layout)

Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout de página**e, em seguida, clique em * * mais Opções de layout * *).
  
## <a name="remarks"></a>Coment�rios

Você também pode definir esse valor na caixa de diálogo **Layout e roteamento espaçamento** (na guia **Design** , clique na seta do grupo **Configurar página** , clique na guia **Layout e roteamento** e clique em **espaçamento**).
  
A grade dinâmica usa a configuração na célula AvenueSizeX quando somente uma forma está disponível para o cálculo de espaçamento horizontal. Para usar a grade dinâmica, na guia **Exibir** , no grupo **Auxílios visuais** , selecione **Grade dinâmica**.
  
Para obter uma referência à célula AvenueSizeX pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | AvenueSizeY  <br/> |
   
Para obter uma referência à célula AvenueSizeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOAvenueSizeX** <br/> |
   

