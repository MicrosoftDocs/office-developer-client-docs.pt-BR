---
title: Célula LineAdjustTo (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm525
localization_priority: Normal
ms.assetid: 81cd9670-8a6f-824b-528c-e9b88c86f525
description: Determina quais conectores dinâmicos são alinhados uns sobre os outros.
ms.openlocfilehash: e4fb32c0fcb488173324ea597edc2c9d13f6bfca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414022"
---
# <a name="lineadjustto-cell-page-layout-section"></a>Célula LineAdjustTo (Seção Page Layout)

Determina quais conectores dinâmicos são alinhados uns sobre os outros.
  
|**Valor**|**Ajuste**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Padrão de estilo de roteamento  <br/> |**visPLOLineAdjustToDefault** <br/> |
|1   <br/> |Linhas próximas umas das outras  <br/> |**visPLOLineAdjustToAll** <br/> |
|2   <br/> |Nenhuma linha  <br/> |**visPLOLineAdjustToNone** <br/> |
|3   <br/> |Linhas relacionadas  <br/> |**visPLOLineAdjustToRelated** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).
  
Para obter uma referência para a célula LineAdjustTo pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |LineAdjustTo  <br/> |
   
Para obter uma referência para a célula LineAdjustTo pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowPageLayout** <br/> |
|Índice de célula:  <br/> |**visPLOLineAdjustTo** <br/> |
   

