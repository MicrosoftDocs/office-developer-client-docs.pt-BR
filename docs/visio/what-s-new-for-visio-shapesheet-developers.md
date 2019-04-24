---
title: Novidades para desenvolvedores do Visio ShapeSheet
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1046253
localization_priority: Normal
ms.assetid: d4f0cf7a-ac4b-c914-7887-e1d65e9d59fa
description: O Visio 2013 fornece uma plataforma única e avançada para suas soluções de desenho personalizadas. Novas células e funções do ShapeSheet, juntamente com novos objetos de automação, propriedades, métodos e eventos, fornecem mais opções para definir e controlar o comportamento dos elementos em suas soluções.
ms.openlocfilehash: 9ab1c447e7cfdf41b8c88a85438ac2904b1395cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297204"
---
# <a name="whats-new-for-visio-shapesheet-developers"></a>Novidades para desenvolvedores do Visio ShapeSheet

O Visio 2013 fornece uma plataforma única e avançada para suas soluções de desenho personalizadas. Novas células e funções do ShapeSheet, juntamente com novos objetos de automação, propriedades, métodos e eventos, fornecem mais opções para definir e controlar o comportamento dos elementos em suas soluções.
  
## <a name="new-and-changed-cells"></a>Células novas e alteradas
<a name="vis15_WhatsNew_Cells"> </a>

A tabela a seguir lista as novas células que você pode usar para criar soluções do ShapeSheet no Visio 2013.
  
|**Nova célula**|**Section**|
|:-----|:-----|
|[BevelBottomHeight](bevelbottomheight-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelBottomType](bevelbottomtype-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelBottomWidth](bevelbottomwidth-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelContourColor](bevelcontourcolor-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelContourSize](bevelcontoursize-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelDepthColor](beveldepthcolor-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelDepthSize](beveldepthsize-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelLightingAngle](bevellightingangle-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelLightingType](bevellightingtype-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelMaterialType](bevelmaterialtype-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelTopHeight](beveltopheight-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelTopType](beveltoptype-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[BevelTopWidth](beveltopwidth-cell-bevel-properties-section.md) <br/> |Propriedades de bisel  <br/> |
|[ClippingPath](clippingpath-cell-foreign-image-info-section.md) <br/> |Informações de imagem estrangeira  <br/> |
|[ColorSchemeIndex](colorschemeindex-cell-theme-properties-section.md) <br/> |Propriedades do tema  <br/> |
|[CompoundType](compoundtype-cell-line-format-section.md) <br/> |Formato de linha  <br/> |
|[ConnectorSchemeIndex](connectorschemeindex-cell-theme-properties-section.md) <br/> |Propriedades do tema  <br/> |
|[DistanceFromGround](distancefromground-cell-3-d-rotation-properties.md) <br/> |Propriedades de rotação 3D  <br/> |
|[DocLockReplace](doclockreplace-cell-document-properties-section.md) <br/> |Propriedades do documento  <br/> |
|[EffectSchemeIndex](effectschemeindex-cell-theme-properties-section.md) <br/> |Propriedades do tema  <br/> |
|[FillGradientAngle](fillgradientangle-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[FillGradientDir](fillgradientdir-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[FillGradientEnabled](fillgradientenabled-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[FontSchemeIndex](fontschemeindex-cell-theme-properties-section.md) <br/> |Propriedades do tema  <br/> |
|[GlowColor](glowcolor-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[GlowColorTrans](glowcolortrans-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[GlowSize](glowsize-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[KeepTextFlat](keeptextflat-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[LineGradientAngle](linegradientangle-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[LineGradientDir](linegradientdir-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[LineGradientEnabled](linegradientenabled-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[LockReplace](lockreplace-cell-protection-section.md) <br/> |Proteção  <br/> |
|[LockThemeConnectors](lockthemeconnectors-cell-protection-section.md) <br/> |Proteção  <br/> |
|[LockThemeFonts](lockthemefonts-cell-protection-section.md) <br/> |Proteção  <br/> |
|[LockThemeIndex](lockthemeindex-cell-protection-section.md) <br/> |Proteção  <br/> |
|[NoCoauth](nocoauth-cell-document-properties-section.md) <br/> |Propriedades do documento  <br/> |
|[PageLockReplace](pagelockreplace-cell-page-properties-section.md) <br/> |Page Properties  <br/> |
|[Perspective](perspective-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[QuickStyleEffectsMatrix](quickstyleeffectsmatrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFillColor](quickstylefillcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFillMatrix](quickstylefillmatrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleFontColor](quickstylefontcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleLineColor](quickstylelinecolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleLineMatrix](quickstylelinematrix-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleShadowColor](quickstyleshadowcolor-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[QuickStyleType](quickstyletype-cell-quick-style-section.md) <br/> |Estilo rápido  <br/> |
|[ReflectionBlur](reflectionblur-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[ReflectionDist](reflectiondist-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[ReflectionSize](reflectionsize-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[ReflectionTrans](reflectiontrans-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md) <br/> |Alterar o comportamento da forma  <br/> |
|[ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md) <br/> |Alterar o comportamento da forma  <br/> |
|[ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md) <br/> |Alterar o comportamento da forma  <br/> |
|[ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) <br/> |Alterar o comportamento da forma  <br/> |
|[RotateGradientWithShape](rotategradientwithshape-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
|[RotationType](rotationtype-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[RotationXAngle](rotationxangle-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[RotationYAngle](rotationyangle-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[RotationZAngle](rotationzangle-cell-3-d-rotation-properties-section.md) <br/> |Propriedades de rotação 3D  <br/> |
|[ShapeShdwBlur](shapeshdwblur-cell-fill-format-section.md) <br/> |Formato de preenchimento  <br/> |
|[ShapeShdwShow](shapeshdwshow-cell-fill-format-section.md) <br/> |Formato de preenchimento  <br/> |
|[SketchAmount](sketchamount-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SketchEnabled](sketchenabled-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SketchFillChange](sketchfillchange-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SketchLineChange](sketchlinechange-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SketchLineWeight](sketchlineweight-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SketchSeed](sketchseed-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[SoftEdgesSize](softedgessize-cell-additional-effect-properties-section.md) <br/> |Propriedades do efeito adicional  <br/> |
|[ThemeIndex](themeindex-cell-theme-properties-section.md) <br/> |Propriedades do tema  <br/> |
|[UseGroupGradient](usegroupgradient-cell-gradient-properties-section.md) <br/> |Propriedades de gradiente  <br/> |
   
A tabela a seguir lista as células que foram alteradas no Visio 2013.
  
|**Célula alterada**|**Anotações**|
|:-----|:-----|
|[ShdwType](shdwtype-cell-page-properties-section.md) <br/> |Novo valor e constante de automação  <br/> |
   
## <a name="new-rows"></a>Novas linhas
<a name="vis15_WhatsNew_Rows"> </a>

A tabela a seguir lista as novas linhas que você pode usar para criar soluções do ShapeSheet no Visio 2013.
  
|**Nova linha**|**Section**|
|:-----|:-----|
|[GradientStop](gradient-stop-row-fill-gradient-section.md) <br/> |Gradiente de preenchimento  <br/> |
|[GradientStop](gradient-stop-row-line-gradient-section.md) <br/> |Gradiente de linha  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Geometria  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Geometria  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Geometria  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Geometria  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Geometria  <br/> |
   
## <a name="new-and-deprecated-functions"></a>Funções novas e preteridas
<a name="vis15_WhatsNew_Functions"> </a>

A tabela a seguir lista as novas funções no Visio 2013.
  
|**Nova função**|
|:-----|
|[NomeDaFonte](font-function.md) <br/> |
|[ISTHEMED](isthemed-function.md) <br/> |
|[PACOTE](language-function.md) <br/> |
|[THEMECBV](themecbv-function.md) <br/> |
||
|[THEMEVAL](themeval-function.md) <br/> |
   
A tabela a seguir lista as funções preteridas no Visio 2013.
  
|**Função preTerida**|**Anotações**|
|:-----|:-----|
|**CELLISTHEMED** <br/> |Substituído por [](isthemed-function.md) função isthemeed.  <br/> |
   

