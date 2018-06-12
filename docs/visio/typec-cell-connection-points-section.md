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
description: Especifica o tipo de ponto de conexão.
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773200"
---
# <a name="type--c-cell-connection-points-section"></a>Célula Type / C (Seção Connection Points)

Especifica o tipo de ponto de conexão.
  
|**Valor**|**Tipo**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Para dentro  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |Para fora  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |DID &amp; para fora  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>Coment�rios

Você também pode definir o tipo de ponto de conexão escolhendo a ferramenta de **conector** , selecionando uma forma e clicando em um ponto de conexão. Para fazer isso, você precisará executar no modo do [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) . 
  
Para obter uma referência para o tipo / C célula pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Connections.Type [ *i* ] onde *i* = < 1 >, 2, 3...  <br/> |
   
Para obter uma referência para o tipo / célula C pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionConnectionPts** <br/> |
|Índice da linha:  <br/> |**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...  <br/> |
|Índice da célula:  <br/> |**visCnnctType** (linhas não-estendidas) **visCnnctC** (linhas estendidas)  <br/> |
   
Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.
  

