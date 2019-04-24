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
description: Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor as formas usando a caixa de diálogo Configurar layout (na guia Design, no grupo layout, clique em reFazer o layout da página e, em seguida, clique em mais opções de layout).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338819"
---
# <a name="avenuesizex-cell-page-layout-section"></a>Célula AvenueSizeX (Seção Page Layout)

Determina a quantidade de espaço horizontal entre as formas na página de desenho ao dispor as formas usando a caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em refazer o **layout da página**e, em seguida, clique em * * mais Opções de layout * *).
  
## <a name="remarks"></a>Comentários

Também é possível definir esse valor na caixa de diálogo **Espaçamento de Layout e Direcionamento** (na guia **Design**, clique na seta do grupo **Configurar Página**, clique na guia **Layout e Direcionamento** e em **Espaçamento**).
  
A grade dinâmica utilizará a configuração na célula AvenueSizeX somente quando uma forma estiver disponível para o cálculo do espaçamento horizontal. Para utilizar a grade dinâmica, na guia **Exibir**, no grupo **Auxílios Visuais**, selecione **Grade Dinâmica**.
  
Para fazer referência à célula AvenueSizeX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | AvenueSizeY  <br/> |
   
Para obter uma referência para a célula AvenueSizeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPageLayout** <br/> |
| Índice da célula:  <br/> |**visPLOAvenueSizeX** <br/> |
   

