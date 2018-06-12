---
title: Célula ShdwScaleFactor (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60083
localization_priority: Normal
ms.assetid: 10979706-6dfe-5241-e862-3f94716d14fa
description: Especifica a porcentagem de aumento ou redução da sombra de uma forma.
ms.openlocfilehash: 99bc48f5332830512e1f5c2f6d93c70b67197c03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772950"
---
# <a name="shdwscalefactor-cell-page-properties-section"></a>Célula ShdwScaleFactor (Seção Page Properties)

Especifica a porcentagem de aumento ou redução da sombra de uma forma. 
  
## <a name="remarks"></a>Comentários

Cada sombra possui um local de pino sombreado, que é um ponto na sombra que corresponde ao pino da forma. Por exemplo, se o pino de uma forma estiver no centro da forma, o local do pino sombreado seria o ponto no centro da sombra. Quando a aplicação da escala em sombras simples, a ampliação é centralizada no local do pino sombreado; Quando a aplicação da escala em sombras oblíquas, ampliação é aplicada na direção oblíqua. 
  
 Esta porcentagem é utilizada quando o tipo de sombra para uma forma é definido como padrão da página (célula ShapeShdwType igual a * * visFSTPageDefault * *). 
  
Para configurar este comportamento para uma forma individual, use a célula ShapeShdwScaleFactor na seção Fill Format.
  
Esse valor corresponde ao valor na caixa **ampliação** da guia **sombras** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). 
  
Para obter uma referência para a célula ShdwScaleFactor pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwScaleFactor  <br/> |
   
Para obter uma referência para a célula ShdwScaleFactor pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwScaleFactor** <br/> |
   

