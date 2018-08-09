---
title: Célula LocalizeMerge (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Determina se as formas são localizadas quando copiadas entre documentos.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772222"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>Célula LocalizeMerge (Seção Miscellaneous)

Determina se as formas são localizadas quando copiadas entre documentos.
  
|**Valor**|**Descrição**|
|:-----|:-----|
| VERDADEIRO  <br/> | Localiza uma forma para o idioma do documento de destino.  <br/> |
| FALSO  <br/> | Não localiza uma forma com base no idioma do documento de destino (o padrão).  <br/> |
   
## <a name="remarks"></a>Comentários

Para fazer referência à célula LocalizeMerge pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | LocalizeMerge  <br/> |
   
Para fazer referência à célula LocalizeMerge pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowMisc** <br/> |
| Índice da célula:  <br/> |**visObjLocalizeMerge** <br/> |
   

