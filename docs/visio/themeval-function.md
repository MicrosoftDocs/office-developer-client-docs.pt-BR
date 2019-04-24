---
title: Função THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Recupera valores do tema ativo.
ms.openlocfilehash: ba95b8a920174ee44c0349d7227258d3ee8a843c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326681"
---
# <a name="themeval-function"></a>Função THEMEVAL

Recupera valores do tema ativo. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMEVAL** ([ _"theme_value"_] [, _padrão_]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Opcional  <br/> |**String** <br/> |O nome de uma célula na definição de tema para obter um valor.  <br/> |
| _default_ <br/> |Opcional  <br/> |Vários  <br/> |Um valor padrão se o documento não tiver temas (não há definição de tema).  <br/> |
   
## <a name="remarks"></a>Comentários

Se a função **THEMEVAL** não receber nenhum argumento, ela retornará o valor com tema da célula host. Este é o valor armazenado na definição do tema atual. A célula host deve ser capaz de ter a capacidade de retornar um valor; se a célula não puder ter sido com o tema, **THEMEVAL** retornará um erro. 
  
Se a função **THEMEVAL** receber um único argumento, ele recuperará o valor da definição de tema passada como o argumento. O argumento passado para o primeiro parâmetro deve ser um inteiro ou uma das cadeias de caracteres exatas listadas na tabela abaixo. 
  
A função **THEMEVAL** também pode aceitar um inteiro para o primeiro parâmetro, como um valor entre 1 e 8. O uso de valores inteiros recupera uma cor por índice a partir do esquema de cores do tema. Portanto, um valor de ' 1 ' retornará a cor "escura" do tema, ' 2 ' retorna a cor "Light", ' 3 ' retorna a cor "ênfase 1", etc. 
  
Se a função **THEMEVAL** receber dois argumentos, ele recuperará o valor da definição de tema passado como o primeiro argumento. No enTanto, se o documento não tiver um tema aplicado a ele, a função **THEMEVAL** usará o valor especificado como o segundo argumento. 
  
**Argumentos possíveis para o parâmetro "theme_value"**

|**Valor**|**Descrição**|
|:-----|:-----|
|Escuríssimo  <br/> |Recupera a cor RGB escura da definição de tema.  <br/> |
|Alegria  <br/> |Recupera a cor RGB claro da definição de tema.  <br/> |
|CorDoFundo  <br/> |Recupera a cor RGB do plano de fundo da definição do tema.  <br/> |
|"AccentColor"  <br/> |Recupera a cor RGB Accent1 da definição de tema.  <br/> |
|"AccentColor2"  <br/> |Recupera a cor RGB Accent2 da definição de tema.  <br/> |
|"AccentColor3"  <br/> |Recupera a cor RGB Accent3 da definição de tema.  <br/> |
|"AccentColor4"  <br/> |Recupera a cor RGB Accent4 da definição de tema.  <br/> |
|"AccentColor5"  <br/> |Recupera a cor RGB Accent5 da definição de tema.  <br/> |
|"AccentColor6"  <br/> |Recupera a cor RGB Accent6 da definição de tema.  <br/> |
|LinePattern  <br/> |Recupera o valor da célula LinePattern da definição de tema.  <br/> |
|Lineweight  <br/> |Recupera o valor da célula espessura da definição de tema.  <br/> |
|LineColor  <br/> |Recupera o valor da célula LineColor da definição de tema.  <br/> |
|LineCap  <br/> |Recupera o valor da célula LineCap da definição de tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula endArrow da definição de tema.  <br/> |
|LineColorTrans  <br/> |Recupera o valor da célula LineColorTrans da definição de tema.  <br/> |
|"LineCompoundtype"  <br/> |Recupera o valor da célula comtralhatype da definição de tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula endArrow da definição de tema.  <br/> |
|"LineBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição de tema.  <br/> |
|"LineEndSize"  <br/> |Recupera o valor de célula endArrows da definição de tema.  <br/> |
|"LineRounding"  <br/> |Recupera o valor de célula de arRedondamento da definição de tema.  <br/> |
|"ConnectorColor"  <br/> |Recupera o valor da célula LineColor da definição de tema.  <br/> |
|"ConnectorPattern"  <br/> |Recupera o valor da célula LinePattern da definição de tema.  <br/> |
|"ConnectorWeight"  <br/> |Recupera o valor da célula espessura da definição de tema.  <br/> |
|"ConnectorTransparency"  <br/> |Recupera o valor da célula LineColorTrans da definição de tema.  <br/> |
|"ConnectorRounding"  <br/> |Recupera o valor de célula de arRedondamento da definição de tema.  <br/> |
|"ConnectorBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"ConnectorEnd"  <br/> |Recupera o valor da célula endArrow da definição de tema.  <br/> |
|"ConnectorBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição de tema.  <br/> |
|"ConnectorEndSize"  <br/> |Recupera o valor de célula endArrows da definição de tema.  <br/> |
|FillColor  <br/> |Recupera o valor da célula FillForegnd da definição de tema.  <br/> |
|"FillColor2"  <br/> |Recupera o valor da célula FillBkgnd da definição de tema.  <br/> |
|"FillTransparency"  <br/> |Recupera o valor da célula FillForegndTrans da definição de tema.  <br/> |
|FillPattern  <br/> |Recupera o valor da célula FillPattern da definição de tema.  <br/> |
|LineGradientEnabled  <br/> |Recupera o valor da célula LineGradientEnabled da definição de tema.  <br/> |
|LineGradientDir  <br/> |Recupera o valor da célula LineGradientDir da definição de tema.  <br/> |
|LineGradientAngle  <br/> |Recupera o valor da célula LineGradientAngle da definição de tema.  <br/> |
|FillGradientEnabled  <br/> |Recupera o valor da célula FillGradientEnabled da definição de tema.  <br/> |
|FillGradientDir  <br/> |Recupera o valor da célula FillGradientDir da definição de tema.  <br/> |
|FillGradientAngle  <br/> |Recupera o valor da célula FillGradientAngle da definição de tema.  <br/> |
|RotateGradientWithShape  <br/> |Recupera o valor da célula RotateGradientWithShape da definição de tema.  <br/> |
|UseGroupGradient  <br/> |Recupera o valor da célula UseGroupGradient da definição de tema.  <br/> |
|"Shadowtype"  <br/> |Recupera o valor da célula ShapeShdwType da definição de tema.  <br/> |
|"ShadowColor"  <br/> |Recupera o valor da célula ShdwColor da definição de tema.  <br/> |
|"ShadowTransparency"  <br/> |Recupera o valor da célula ShdwColorTrans da definição de tema.  <br/> |
|"ShadowMagnification"  <br/> |Recupera o valor da célula ShapeShdwScaleFactor da definição de tema.  <br/> |
|"ShadowBlur"  <br/> |Recupera o valor da célula ShapeShdwBlur da definição de tema.  <br/> |
|"ShadowXOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetX da definição de tema.  <br/> |
|"ShadowYOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetY da definição de tema.  <br/> |
|"ShadowDirection"  <br/> |Recupera o valor da célula ShapeShdwObliqueAngle da definição de tema.  <br/> |
|"ShadowPattern"  <br/> |Recupera o valor da célula ShdwPattern da definição de tema.  <br/> |
|BevelTopType  <br/> |Recupera o valor da célula BevelTopType da definição de tema.  <br/> |
|BevelTopWidth  <br/> |Recupera o valor da célula BevelTopWidth da definição de tema.  <br/> |
|BevelTopHeight  <br/> |Recupera o valor da célula BevelTopHeight da definição de tema.  <br/> |
|"BevelMaterial"  <br/> |Recupera o valor da célula BevelMaterialType da definição de tema.  <br/> |
|"BevelLighting"  <br/> |Recupera o valor da célula BevelLightingType da definição de tema.  <br/> |
|BevelLightingAngle  <br/> |Recupera o valor da célula BevelLightingAngle da definição de tema.  <br/> |
|BevelContourColor  <br/> |Recupera o valor da célula BevelContourColor da definição de tema.  <br/> |
|BevelContourSize  <br/> |Recupera o valor da célula BevelContourSize da definição de tema.  <br/> |
|ReflectionBlur  <br/> |Recupera o valor da célula ReflectionBlur da definição de tema.  <br/> |
|ReflectionDist  <br/> |Recupera o valor da célula ReflectionDist da definição de tema.  <br/> |
|ReflectionSize  <br/> |Recupera o valor de célula de reflexões da definição de tema.  <br/> |
|ReflectionTrans  <br/> |Recupera o valor da célula ReflectionTrans da definição de tema.  <br/> |
|SoftEdgesSize  <br/> |Recupera o valor da célula SoftEdgesSize da definição de tema.  <br/> |
|GlowSize  <br/> |Recupera o valor da célula GlowSize da definição de tema.  <br/> |
|GlowColor  <br/> |Recupera o valor da célula GlowColor da definição de tema.  <br/> |
|"GlowTransparency"  <br/> |Recupera o valor da célula GlowColorTrans da definição de tema.  <br/> |
|SketchAmount  <br/> |Recupera o valor da célula SketchAmount da definição de tema.  <br/> |
|SketchEnabled  <br/> |Recupera o valor da célula SketchEnabled da definição de tema.  <br/> |
|SketchFillChange  <br/> |Recupera o valor da célula SketchFillChange da definição de tema.  <br/> |
|SketchLineChange  <br/> |Recupera o valor da célula SketchLineChange da definição de tema.  <br/> |
|SketchLineWeight  <br/> |Recupera o valor da célula SketchLineWeight da definição de tema.  <br/> |
|"LatinFont"  <br/> |Recupera o valor da célula Font da definição de tema.  <br/> |
|TextColor  <br/> |Recupera o valor de célula Color da definição de tema.  <br/> |
|TextStyle  <br/> |Recupera o valor da célula Character. Style da definição de tema.  <br/> |
|"ComplexFont"  <br/> |Recupera o valor da célula ComplexScriptFont da definição de tema.  <br/> |
|AsianFont  <br/> |Recupera o valor da célula AsianFont da definição de tema.  <br/> |
|"FillStop [x] Color"  <br/> |Recupera o valor da célula Color na linha *x* da definição do tema.  <br/> |
|"FillStop [x] transparência"  <br/> |Recupera o valor da célula ColorTrans na linha *x* da definição do tema.  <br/> |
|"FillStop [x] position"  <br/> |Recupera o valor da célula position na linha *x* da definição do tema.  <br/> |
|"LineStop [x] Color"  <br/> |Recupera o valor da célula Color na linha *x* da definição do tema.  <br/> |
|"LineStop [x] transparência"  <br/> |Recupera o valor da célula ColorTrans na linha *x* da definição do tema.  <br/> |
|"LineStop [x] position"  <br/> |Recupera o valor da célula position na linha *x* da definição do tema.  <br/> |
   
## <a name="example"></a>Exemplo

 `THEMEVAL("5")`
  
Retorna a cor "ênfase 3" da definição de tema.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Retorna o valor da célula "espessura" da definição de tema. Se a forma que contém essa função não tiver nenhum tema aplicado a ela, a função retornará ' 0,7 pt. '.
  

