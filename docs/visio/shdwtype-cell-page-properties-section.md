---
title: Célula ShdwType (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indica o tipo de sombra padrão para uma página.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772959"
---
# <a name="shdwtype-cell-page-properties-section"></a>Célula ShdwType (Seção Page Properties)

Indica o tipo de sombra padrão para uma página.
  
|**Valor**|**Descrição**|**Constante de automação**|
|:-----|:-----|:-----|
| 1  <br/> | Simples  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Oblíquo  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Interna  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Coment�rios

 O tipo de sombra descrito nesta célula é utilizado sempre que a célula ShapeShdwType (o tipo de sombra para uma forma individual na página) for definida como padrão da página (**visFSTPageDefault** ). 
  
Tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI). Uma sombra simples dá o efeito da forma sendo sombreada em um plano paralelo localizado um pouco atrás dela. Sombras oblíquas são descritas como sombras oblíquas na interface de usuário e fornecer o efeito de uma sombra sendo convertida em um plano perpendicular à forma. 
  
Para obter uma lista dos tipos de sombra de simples e oblíqua predefinidos, consulte a lista de **estilo** na guia **sombras** da caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ). 
  
Para obter uma referência à célula ShdwType pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize: 
  
|||
|:-----|:-----|
| Nome da célula:  <br/> | ShdwType  <br/> |
   
Para obter uma referência para a célula ShapeShdwOffsetX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos: 
  
|||
|:-----|:-----|
| Índice da seção:  <br/> |**visSectionObject** <br/> |
| Índice da linha:  <br/> |**visRowPage** <br/> |
| Índice da célula:  <br/> |**visPageShdwType** <br/> |
   

