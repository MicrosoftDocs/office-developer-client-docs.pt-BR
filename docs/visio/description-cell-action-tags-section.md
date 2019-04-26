---
title: Célula Description (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360225"
---
# <a name="description-cell-action-tags-section"></a>Célula de Descrição (Seção Ação Marcas)

Contém uma cadeia de caracteres que descreve a marca de ação, que aparece como uma dica de ferramenta quando os usuários colocam o ponteiro sobre a marca.
  
## <a name="remarks"></a>Comentários

Para obter uma referência à célula Descrição pelo nome de outra fórmula ou por um programa que utiliza a propriedade **CellsU**, use: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | SmartTags.  *nome*  .Descrição           onde MarcasInteligentes. *nome*  é o nome da linha da marca de ação  <br/> |
   
Para obter uma referência à célula Description pelo índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionSmartTag** <br/> |
| Índice de linha:  <br/> |**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...  <br/> |
| Índice de célula:  <br/> |**visSmartTagDescription** <br/> |
   

