---
title: Célula Type / C (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: Determina o tipo de ponto de conexão.
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415233"
---
# <a name="type--c-cell-connection-points-section"></a>Célula Type / C (Seção Connection Points)

Determina o tipo de ponto de conexão.
  
|**Valor**|**Tipo**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Para dentro  <br/> |**visCnnctTypeInward** <br/> |
|1   <br/> |Para fora  <br/> |**visCnnctTypeOutward** <br/> |
|2   <br/> |Para dentro &amp; para fora  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Comentários

Também é possível definir o tipo de ponto de conexão escolhendo a ferramenta **Conector**, selecionando uma forma e clicando com o botão direito do mouse em um ponto de conexão. Para fazer isso, você precisa executar no modo do [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md). 
  
Para obter uma referência para a célula Type / C pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Connections.Type[  *i*  ] onde i =  *<*  1>, 2, 3...  <br/> |
   
Para obter uma referência para a célula Type / C pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
|Índice de linha:  <br/> |**visRowConnectionPts**  +   *i* onde *i* = 0, 1, 2...  <br/> |
|Índice de célula:  <br/> |**visCnnctType** (linhas não estendidas) **visCnnctC** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

