---
title: Célula ObjType (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Determina se os objetos são de colocação ou se podem ser roteados em diagramas quando você usa a caixa de diálogo Configurar Layout para dispor formas.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772441"
---
# <a name="objtype-cell-miscellaneous-section"></a>Célula ObjType (Seção Miscellaneous)

Determina se os objetos são de colocação ou se podem ser roteados em diagramas quando você usa a caixa de diálogo **Configurar Layout** para dispor formas. 
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |Padrão. O aplicativo decide com base no contexto do desenho.  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |A forma é de colocação.  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |A forma pode ser roteada. Deve ser uma forma unidimensional (1D).  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |A forma não é de colocação e não pode ser roteada.  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |O grupo contém formas de colocação e que podem ser roteadas.  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>Comentários

Como padrão, a célula ObjType está definida para uma forma como No Formula, cuja avaliação é 0, o que significa que o aplicativo irá determinar se a forma pode ser de colocação de acordo com seu contexto. Por exemplo, se você desenhar um simples retângulo, o valor de sua célula ObjType será 0. Em seguida, se você utilizar a ferramenta **Conector** para conectar o retângulo a outra forma, o Visio redefinirá o valor da célula ObjType do retângulo para 1 (de colocação). 
  
O valor da célula ObjType pode ser uma combinação dos valores. Se o bit não seja de colocação for definido (&amp;H4), no entanto, terá precedência sobre outros valores, exceto o valor de grupo (&amp;H8).
  
Para obter uma referência para a célula ObjType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |ObjType  <br/> |
   
Para obter uma referência para a célula ObjType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowMisc** <br/> |
|Índice da célula:  <br/> |**visLOFlags** <br/> |
   

