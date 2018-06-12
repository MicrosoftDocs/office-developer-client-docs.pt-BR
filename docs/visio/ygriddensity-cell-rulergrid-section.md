---
title: Célula YGridDensity (seção Ruler &amp; seção grade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Especifica o tipo de grade vertical a ser utilizada.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773339"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a>Célula YGridDensity (seção Ruler &amp; seção grade)

Especifica o tipo de grade vertical a ser utilizada.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixa  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grande  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (padrão)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Pequena  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa célula corresponde ao **espaçamento da grade** vertical opção no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência à célula YGridDensity pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |YGridDensity  <br/> |
   
Para obter uma referência à célula YGridDensity pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visYGridDensity** <br/> |
   

