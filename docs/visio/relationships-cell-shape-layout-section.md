---
title: Célula Relationships (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Armazena as relações entre contêineres, listas, textos explicativos e formas.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406406"
---
# <a name="relationships-cell-shape-layout-section"></a>Célula Relationships (Seção Shape Layout)

Armazena as relações entre contêineres, listas, textos explicativos e formas. 
  
## <a name="remarks"></a>Comentários

 O Microsoft Visio usa a célula relações para armazenar as relações que envolvem essa forma. Uma série de funções DEPENDSON, com os parâmetros mostrados, são usadas para representar relações com essa forma, como apresentado na tabela a seguir. 
  
|**Primeiro parâmetro**|**Parâmetros adicionais**|
|:-----|:-----|
|1  <br/> |Formas que são membros deste contêiner.  <br/> |
|duas  <br/> |Formas que são membros desta lista.  <br/> |
|3D  <br/> |Textos explicativos que estão associados a esta forma.  <br/> |
|4   <br/> |Contêneres dos quais esta forma é membro.  <br/> |
|5   <br/> |Lista da qual este item de lista é membro.  <br/> |
|6   <br/> |Forma associada a este texto explicativo.  <br/> |
|7   <br/> |Contêiner na borda limítrofe esquerda da qual esta forma é membro.  <br/> |
|8   <br/> |Contêiner na borda limítrofe direita da qual esta forma é membro.  <br/> |
|9   <br/> |Contêiner na borda limítrofe superior da qual esta forma é membro.  <br/> |
|10   <br/> |Contêiner na borda limítrofe inferior da qual esta forma é membro.  <br/> |
|11   <br/> |Lista à qual esta lista se sobrepõe.  <br/> |
   
Para obter uma referência à célula Relationships pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Relações  <br/> |
   
Para obter uma referência à célula Relationships pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice de linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice de célula:  <br/> |**visSLORelationships** <br/> |
   

