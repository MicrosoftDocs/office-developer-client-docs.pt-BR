---
title: Célula LineAdjustFrom (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251887
localization_priority: Normal
ms.assetid: 6949c717-dc69-1d17-5215-eb6efce56fcb
description: Determina quais conectores dinâmicos serão separados pelos espaços do aplicativo se forem roteados uns sobre os outros.
ms.openlocfilehash: ee3a107f7e19b53017c2ea24c94babceb49620d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772182"
---
# <a name="lineadjustfrom-cell-page-layout-section"></a>Célula LineAdjustFrom (Seção Page Layout)

Determina quais conectores dinâmicos serão separados pelos espaços do aplicativo se forem roteados uns sobre os outros.
  
|**Valor**|**Ajuste**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Linhas não relacionadas  <br/> |**visPLOLineAdjustFromNotRelated** <br/> |
|1  <br/> |Todas as linhas  <br/> |**visPLOLineAdjustFromAll** <br/> |
|2  <br/> |Nenhuma linha  <br/> |**visPLOLineAdjustFromNone** <br/> |
|3  <br/> |Padrão de estilo de roteamento  <br/> |**visPLOLineAdjustFromRoutingDefault** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência para a célula LineAdjustFrom pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineAdjustFrom  <br/> |
   
Para obter uma referência para a célula LineAdjustFrom pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowPageLayout** <br/> |
|Índice da célula:  <br/> |**visPLOLineAdjustFrom** <br/> |
   

