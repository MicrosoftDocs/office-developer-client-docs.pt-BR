---
title: Célula Value (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: Contém o valor do item de dados de forma como inserido na caixa de diálogo Definir dados da forma.
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773251"
---
# <a name="value-cell-shape-data-section"></a>Célula Value (Seção Shape Data)

Contém o valor do item de dados de forma como inserido na caixa de diálogo **Definir dados da forma** . 
  
## <a name="remarks"></a>Coment�rios

As fórmulas inseridas nesta célula são substituídas por valores inseridos na caixa de diálogo **Definir dados da forma** . Isso ocorre mesmo que você use a função GUARD para proteger a fórmula. 
  
Para obter uma referência à célula Value pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | Prop.  *Nome* . Valor onde Prop.  *Name* é o nome da linha  <br/> |
   
Para obter uma referência à célula Value pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionProp** <br/> |
| Índice da linha:  <br/> |**visRowProp** +  *i* onde *i* = 0, 1, 2...  <br/> |
| Índice da célula:  <br/> |**visCustPropsValue** <br/> |
   

