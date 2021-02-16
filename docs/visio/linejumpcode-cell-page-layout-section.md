---
title: Célula LineJumpCode (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm540
localization_priority: Normal
ms.assetid: 56f9043d-a632-65df-c710-45867cce1627
description: Determina os conectores aos quais você deseja adicionar saltos.
ms.openlocfilehash: 7b5b8c8f1de160a4dc766d30a5f518c5653c270b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416248"
---
# <a name="linejumpcode-cell-page-layout-section"></a>Célula LineJumpCode (Seção Page Layout)

Determina os conectores aos quais você deseja adicionar saltos.
  
|**Valor**|**Conectores aos quais você deseja adicionar saltos**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Nenhum  <br/> |**visPLOJumpNone** <br/> |
|1   <br/> |Linhas horizontais  <br/> |**visPLOJumpHorizontal** <br/> |
|2   <br/> |Linhas verticais  <br/> |**visPLOJumpVertical** <br/> |
|3   <br/> |Última linha circulada  <br/> |**visPLOJumpLastRouted** <br/> |
|4   <br/> |Última linha exibida (forma superior na ordem *z)*  <br/> |**visPLOJumpDisplayOrder** <br/> |
|5   <br/> |Primeira linha exibida (forma na parte inferior da ordem *z)*  <br/> |**visPLOJumpReverseDisplayOrder** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência para a célula LineJumpCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineJumpCode  <br/> |
   
Para obter uma referência para a célula LineJumpCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice de célula:  <br/> |**visPLOJumpCode** <br/> |
   

