---
title: Célula XGridDensity (seção Ruler &amp; seção grade)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Especifica o tipo de grade horizontal a ser utilizada.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773309"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a>Célula XGridDensity (seção Ruler &amp; seção grade)

Especifica o tipo de grade horizontal a ser utilizada.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
|0  <br/> |Fixa  <br/> |**visGridFixed** <br/> |
|2  <br/> |Grande  <br/> |**visGridCoarse** <br/> |
|4  <br/> |Normal (padrão)  <br/> |**visGridNormal** <br/> |
|8  <br/> |Pequena  <br/> |**visGridFine** <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa célula corresponde ao **espaçamento da grade** horizontal opção no **régua &amp; grade** caixa de diálogo (na guia **Exibir** , clique na seta **Mostrar** ). 
  
Para obter uma referência para a célula XGridDensity pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
|Nome da célula:  <br/> |XGridDensity  <br/> |
   
Para obter uma referência para a célula XGridDensity pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
|Índice da seção:  <br/> |**visSectionObject** <br/> |
|Índice da linha:  <br/> |**visRowRulerGrid** <br/> |
|Índice da célula:  <br/> |**visXGridDensity** <br/> |
   

