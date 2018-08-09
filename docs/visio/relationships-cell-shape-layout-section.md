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
ms.openlocfilehash: c3410ad15581ff1704d7a43dd7ed5fa193f668b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772676"
---
# <a name="relationships-cell-shape-layout-section"></a>Célula Relationships (Seção Shape Layout)

Armazena as relações entre contêineres, listas, textos explicativos e formas. 
  
## <a name="remarks"></a>Comentários

 Microsoft Visio usa a célula Relationships para armazenar as relações que envolvem esta forma. Uma série de funções DEPENDSON, com os parâmetros mostrados, são usados para representar os relacionamentos com esta forma, conforme mostrado na tabela a seguir. 
  
|**Primeiro parâmetro**|**Parâmetros adicionais**|
|:-----|:-----|
|1  <br/> |Formas que são membros deste contêiner.  <br/> |
|2  <br/> |Formas que são membros desta lista.  <br/> |
|3  <br/> |Textos explicativos que estão associados a esta forma.  <br/> |
|4  <br/> |Contêneres dos quais esta forma é membro.  <br/> |
|5  <br/> |Lista da qual este item de lista é membro.  <br/> |
|6  <br/> |Forma associada a este texto explicativo.  <br/> |
|7  <br/> |Contêiner na borda limítrofe esquerda da qual esta forma é membro.  <br/> |
|8  <br/> |Contêiner na borda limítrofe direita da qual esta forma é membro.  <br/> |
|9  <br/> |Contêiner na borda limítrofe superior da qual esta forma é membro.  <br/> |
|10  <br/> |Contêiner na borda limítrofe inferior da qual esta forma é membro.  <br/> |
|11  <br/> |Lista à qual esta lista se sobrepõe.  <br/> |
   
Para obter uma referência à célula Relationships pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |Relações  <br/> |
   
Para obter uma referência à célula Relationships pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowShapeLayout** <br/> |
|Índice da célula:  <br/> |**visSLORelationships** <br/> |
   

