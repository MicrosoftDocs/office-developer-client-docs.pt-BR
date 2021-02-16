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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415751"
---
# <a name="themeval-function"></a>Função THEMEVAL

Recupera valores do tema ativo. 
  
## <a name="version-information"></a>Informações sobre a versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMEVAL**([ _"theme_value"_][, _padrão_]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Opcional  <br/> |**String** <br/> |O nome de uma célula na definição do tema para obter um valor.  <br/> |
| _default_ <br/> |Opcional  <br/> |Vários  <br/> |Um valor padrão se o documento não tiver temas (não há definição de tema).  <br/> |
   
## <a name="remarks"></a>Comentários

Se a **função THEMEVAL** não receber argumentos, ela retornará o valor com tema da célula host. Esse é o valor armazenado na definição do tema atual. A célula host deve ser capaz de ter temas para retornar um valor; se a célula não for capaz de ter temas, **THEMEVAL** retornará um erro. 
  
Se a **função THEMEVAL** receber um único argumento, ela recuperará o valor da definição de tema passada como o argumento. O argumento passado para o primeiro parâmetro deve ser um inteiro ou uma das cadeias de caracteres exatas listadas na tabela abaixo. 
  
A **função THEMEVAL** também pode aceitar um inteiro para o primeiro parâmetro, como um valor entre 1 e 8. O uso de valores inteiros recupera uma cor pelo índice do esquema de cores do tema. Assim, um valor de '1' retornará a cor "Escuro" do tema, "2" retornará a cor "Claro", "3" retornará a cor "Ênfase 1", etc. 
  
Se a **função THEMEVAL** receber dois argumentos, ela recuperará o valor da definição de tema passada como o primeiro argumento. No entanto, se o documento não tiver tema aplicado a ele, a função **THEMEVAL** usará o valor especificado como o segundo argumento. 
  
**Argumentos possíveis para o parâmetro "theme_value"**

|**Valor**|**Descrição**|
|:-----|:-----|
|"Dark"  <br/> |Recupera a cor RGB Escura da definição do tema.  <br/> |
|"Light"  <br/> |Recupera a cor RGB claro da definição do tema.  <br/> |
|"BackgroundColor"  <br/> |Recupera a cor RGB do plano de fundo da definição do tema.  <br/> |
|"AccentColor"  <br/> |Recupera a cor RGB Accent1 da definição do tema.  <br/> |
|"AccentColor2"  <br/> |Recupera a cor RGB Accent2 da definição do tema.  <br/> |
|"AccentColor3"  <br/> |Recupera a cor RGB Accent3 da definição do tema.  <br/> |
|"AccentColor4"  <br/> |Recupera a cor RGB Accent4 da definição do tema.  <br/> |
|"AccentColor5"  <br/> |Recupera a cor RGB Accent5 da definição do tema.  <br/> |
|"AccentColor6"  <br/> |Recupera a cor RGB Accent6 da definição do tema.  <br/> |
|"LinePattern"  <br/> |Recupera o valor da célula LinePattern da definição do tema.  <br/> |
|"LineWeight"  <br/> |Recupera o valor da célula LineWeight da definição do tema.  <br/> |
|"LineColor"  <br/> |Recupera o valor da célula LineColor da definição do tema.  <br/> |
|"LineCap"  <br/> |Recupera o valor da célula LineCap da definição do tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição do tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula EndArrow da definição do tema.  <br/> |
|"LineColorTrans"  <br/> |Recupera o valor da célula LineColorTrans da definição do tema.  <br/> |
|"LineCompoundtype"  <br/> |Recupera o valor da célula CompoundType da definição do tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição do tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula EndArrow da definição do tema.  <br/> |
|"LineBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição do tema.  <br/> |
|"LineEndSize"  <br/> |Recupera o valor da célula EndArrowSize da definição do tema.  <br/> |
|"LineRounding"  <br/> |Recupera o valor da célula Rounding da definição do tema.  <br/> |
|"ConnectorColor"  <br/> |Recupera o valor da célula LineColor da definição do tema.  <br/> |
|"ConnectorPattern"  <br/> |Recupera o valor da célula LinePattern da definição do tema.  <br/> |
|"ConnectorWeight"  <br/> |Recupera o valor da célula LineWeight da definição do tema.  <br/> |
|"ConnectorTransparency"  <br/> |Recupera o valor da célula LineColorTrans da definição do tema.  <br/> |
|"ConnectorRounding"  <br/> |Recupera o valor da célula Rounding da definição do tema.  <br/> |
|"ConnectorBegin"  <br/> |Recupera o valor da célula BeginArrow da definição do tema.  <br/> |
|"ConnectorEnd"  <br/> |Recupera o valor da célula EndArrow da definição do tema.  <br/> |
|"ConnectorBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição do tema.  <br/> |
|"ConnectorEndSize"  <br/> |Recupera o valor da célula EndArrowSize da definição do tema.  <br/> |
|"FillColor"  <br/> |Recupera o valor da célula FillForegnd a partir da definição do tema.  <br/> |
|"FillColor2"  <br/> |Recupera o valor da célula FillBkgnd da definição do tema.  <br/> |
|"FillTransparency"  <br/> |Recupera o valor da célula FillForegndTrans da definição do tema.  <br/> |
|"FillPattern"  <br/> |Recupera o valor da célula FillPattern da definição do tema.  <br/> |
|"LineGradientEnabled"  <br/> |Recupera o valor da célula LineGradientEnabled da definição do tema.  <br/> |
|"LineGradientDir"  <br/> |Recupera o valor da célula LineGradientDir da definição do tema.  <br/> |
|"LineGradientAngle"  <br/> |Recupera o valor da célula LineGradientAngle a partir da definição do tema.  <br/> |
|"FillGradientEnabled"  <br/> |Recupera o valor da célula FillGradientEnabled da definição do tema.  <br/> |
|"FillGradientDir"  <br/> |Recupera o valor da célula FillGradientDir da definição do tema.  <br/> |
|"FillGradientAngle"  <br/> |Recupera o valor da célula FillGradientAngle a partir da definição do tema.  <br/> |
|"RotateGradientWithShape"  <br/> |Recupera o valor da célula RotateGradientWithShape da definição do tema.  <br/> |
|"UseGroupGradient"  <br/> |Recupera o valor da célula UseGroupGradient da definição do tema.  <br/> |
|"ShadowType"  <br/> |Recupera o valor da célula ShapeShdwType da definição do tema.  <br/> |
|"ShadowColor"  <br/> |Recupera o valor da célula ShdwColor da definição do tema.  <br/> |
|"ShadowTransparency"  <br/> |Recupera o valor da célula ShdwColorTrans da definição do tema.  <br/> |
|"ShadowMagnification"  <br/> |Recupera o valor da célula ShapeShdwScaleFactor da definição do tema.  <br/> |
|"ShadowBlur"  <br/> |Recupera o valor da célula ShapeShdwBlur da definição do tema.  <br/> |
|"ShadowXOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetX da definição do tema.  <br/> |
|"ShadowYOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetY da definição do tema.  <br/> |
|"ShadowDirection"  <br/> |Recupera o valor da célula ShapeShdwObliqueAngle da definição do tema.  <br/> |
|"ShadowPattern"  <br/> |Recupera o valor da célula ShdwPattern da definição do tema.  <br/> |
|"BevelTopType"  <br/> |Recupera o valor da célula BevelTopType da definição do tema.  <br/> |
|"BevelTopWidth"  <br/> |Recupera o valor da célula BevelTopWidth da definição do tema.  <br/> |
|"BevelTopHeight"  <br/> |Recupera o valor da célula BevelTopHeight da definição do tema.  <br/> |
|"BevelMaterial"  <br/> |Recupera o valor da célula BevelMaterialType da definição do tema.  <br/> |
|"BevelLighting"  <br/> |Recupera o valor da célula BevelLightingType da definição do tema.  <br/> |
|"BevelLightingAngle"  <br/> |Recupera o valor da célula BevelLightingAngle da definição do tema.  <br/> |
|"BevelContourColor"  <br/> |Recupera o valor da célula BevelContourColor da definição do tema.  <br/> |
|"BevelContourSize"  <br/> |Recupera o valor da célula BevelContourSize da definição do tema.  <br/> |
|"ReflectionBlur"  <br/> |Recupera o valor da célula ReflectionBlur da definição do tema.  <br/> |
|"ReflectionDist"  <br/> |Recupera o valor da célula ReflectionDist da definição do tema.  <br/> |
|"ReflectionSize"  <br/> |Recupera o valor da célula ReflectionSize da definição do tema.  <br/> |
|"ReflectionTrans"  <br/> |Recupera o valor da célula ReflectionTrans da definição do tema.  <br/> |
|"SoftEdgesSize"  <br/> |Recupera o valor da célula SoftEdgesSize da definição do tema.  <br/> |
|"GlowSize"  <br/> |Recupera o valor da célula GlowSize da definição do tema.  <br/> |
|"GlowColor"  <br/> |Recupera o valor da célula GlowColor da definição do tema.  <br/> |
|"GlowTransparency"  <br/> |Recupera o valor da célula GlowColorTrans da definição do tema.  <br/> |
|"SketchAmount"  <br/> |Recupera o valor da célula SketchAmount da definição do tema.  <br/> |
|"SketchEnabled"  <br/> |Recupera o valor da célula SketchEnabled da definição do tema.  <br/> |
|"SketchFillChange"  <br/> |Recupera o valor da célula SketchFillChange a partir da definição do tema.  <br/> |
|"SketchLineChange"  <br/> |Recupera o valor da célula SketchLineChange da definição do tema.  <br/> |
|"SketchLineWeight"  <br/> |Recupera o valor da célula SketchLineWeight da definição do tema.  <br/> |
|"LatinFont"  <br/> |Recupera o valor da célula Font da definição do tema.  <br/> |
|"TextColor"  <br/> |Recupera o valor da célula Color da definição do tema.  <br/> |
|"TextStyle"  <br/> |Recupera o valor da célula Character.Style da definição do tema.  <br/> |
|"ComplexFont"  <br/> |Recupera o valor da célula ComplexScriptFont da definição do tema.  <br/> |
|"AsianFont"  <br/> |Recupera o valor da célula AsianFont da definição do tema.  <br/> |
|"FillStop[x]Color"  <br/> |Recupera o valor da célula Color na linha  *x da*  definição do tema.  <br/> |
|"FillStop[x]Transparency"  <br/> |Recupera o valor da célula ColorTrans na linha  *x da*  definição do tema.  <br/> |
|"FillStop[x]Position"  <br/> |Recupera o valor da célula Position na linha  *x da*  definição do tema.  <br/> |
|"LineStop[x]Color"  <br/> |Recupera o valor da célula Color na linha  *x da*  definição do tema.  <br/> |
|"LineStop[x]Transparency"  <br/> |Recupera o valor da célula ColorTrans na linha  *x da*  definição do tema.  <br/> |
|"LineStop[x]Position"  <br/> |Recupera o valor da célula Position na linha  *x da*  definição do tema.  <br/> |
   
## <a name="example"></a>Exemplo

 `THEMEVAL("5")`
  
Retorna a cor "Ênfase 3" da definição do tema.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Retorna o valor da célula "LineWeight" da definição do tema. Se a forma que contém essa função não tiver tema aplicado a ela, a função retornará '0,7 pt.'.
  

