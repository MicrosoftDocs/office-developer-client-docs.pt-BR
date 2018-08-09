---
title: Função THEMEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eac3b8c-532c-4312-935d-fe8b63bcaf75
description: Recupera os valores do tema ativo.
ms.openlocfilehash: 7bbd017c859a0a167bbd279d60af029e98421375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773146"
---
# <a name="themeval-function"></a>Função THEMEVAL

Recupera os valores do tema ativo. 
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2013
 
  
## <a name="syntax"></a>Sintaxe

 **THEMEVAL** ([ _"theme_value"_] [, _padrão_]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _"theme_value"_ <br/> |Opcional  <br/> |**String** <br/> |O nome de uma célula na definição de tema para obter um valor de.  <br/> |
| _default_ <br/> |Opcional  <br/> |Vários  <br/> |Um valor padrão se o documento não estiver com tema (não há uma definição de tema).  <br/> |
   
## <a name="remarks"></a>Comentários

Se a função **THEMEVAL** não receber nenhum argumento, ele retornará o valor com temas da célula host. Este é o valor armazenado na definição de tema atual. A célula do host deve ser capaz de sendo com temas, para retornar um valor; Se a célula não é capaz de sendo com temas, **THEMEVAL** retornará um erro. 
  
Se a função **THEMEVAL** recebe um único argumento, ele recupera o valor da definição de tema passada como o argumento. O argumento passado para o primeiro parâmetro deve ser um inteiro ou uma das cadeias de caracteres exatas listadas na tabela a seguir. 
  
A função **THEMEVAL** também pode aceitar um número inteiro para o primeiro parâmetro, como um valor entre 1 e 8. Usar valores inteiros recupera uma cor pelo índice a partir do esquema de cores do tema. Assim, um valor de '1' retornará a "Escura" cor do tema, '2' Retorna a cor de "Claro", '3' Retorna a cor "Ênfase 1", etc. 
  
Se a função **THEMEVAL** recebe dois argumentos, ele recupera o valor da definição de tema passada como o primeiro argumento. No entanto, se o documento tiver sem tema aplicado a ela, a função **THEMEVAL** usa o valor especificado como o segundo argumento. 
  
**Argumentos possíveis para o parâmetro "theme_value"**

|**Valor**|**Descrição**|
|:-----|:-----|
|"Escuro"  <br/> |Recupera a cor RGB escuro da definição de tema.  <br/> |
|"Claro"  <br/> |Recupera a cor RGB claro da definição de tema.  <br/> |
|"BackgroundColor"  <br/> |Recupera a cor de plano de fundo RGB da definição de tema.  <br/> |
|"AccentColor"  <br/> |Recupera a cor de Ênfase 1 RGB da definição de tema.  <br/> |
|"AccentColor2"  <br/> |Recupera a cor RGB Accent2 da definição de tema.  <br/> |
|"AccentColor3"  <br/> |Recupera a cor RGB Accent3 da definição de tema.  <br/> |
|"AccentColor4"  <br/> |Recupera a cor RGB Accent4 da definição de tema.  <br/> |
|"AccentColor5"  <br/> |Recupera a cor RGB Accent5 da definição de tema.  <br/> |
|"AccentColor6"  <br/> |Recupera a cor RGB Accent6 da definição de tema.  <br/> |
|"LinePattern"  <br/> |Recupera o valor da célula LinePattern da definição de tema.  <br/> |
|"LineWeight"  <br/> |Recupera o valor da célula LineWeight da definição de tema.  <br/> |
|"LineColor"  <br/> |Recupera o valor da célula LineColor da definição de tema.  <br/> |
|"LineCap"  <br/> |Recupera o valor da célula LineCap da definição de tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula EndArrow da definição de tema.  <br/> |
|"LineColorTrans"  <br/> |Recupera o valor da célula LineColorTrans da definição de tema.  <br/> |
|"LineCompoundtype"  <br/> |Recupera o valor da célula CompoundType da definição de tema.  <br/> |
|"LineBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"LineEnd"  <br/> |Recupera o valor da célula EndArrow da definição de tema.  <br/> |
|"LineBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição de tema.  <br/> |
|"LineEndSize"  <br/> |Recupera o valor da célula EndArrowSize da definição de tema.  <br/> |
|"LineRounding"  <br/> |Recupera o valor da célula Rounding da definição de tema.  <br/> |
|"ConnectorColor"  <br/> |Recupera o valor da célula LineColor da definição de tema.  <br/> |
|"ConnectorPattern"  <br/> |Recupera o valor da célula LinePattern da definição de tema.  <br/> |
|"ConnectorWeight"  <br/> |Recupera o valor da célula LineWeight da definição de tema.  <br/> |
|"ConnectorTransparency"  <br/> |Recupera o valor da célula LineColorTrans da definição de tema.  <br/> |
|"ConnectorRounding"  <br/> |Recupera o valor da célula Rounding da definição de tema.  <br/> |
|"ConnectorBegin"  <br/> |Recupera o valor da célula BeginArrow da definição de tema.  <br/> |
|"ConnectorEnd"  <br/> |Recupera o valor da célula EndArrow da definição de tema.  <br/> |
|"ConnectorBeginSize"  <br/> |Recupera o valor da célula BeginArrowSize da definição de tema.  <br/> |
|"ConnectorEndSize"  <br/> |Recupera o valor da célula EndArrowSize da definição de tema.  <br/> |
|"FillColor"  <br/> |Recupera o valor da célula FillForegnd da definição de tema.  <br/> |
|"FillColor2"  <br/> |Recupera o valor da célula FillBkgnd da definição de tema.  <br/> |
|"FillTransparency"  <br/> |Recupera o valor da célula FillForegndTrans da definição de tema.  <br/> |
|"FillPattern"  <br/> |Recupera o valor da célula FillPattern da definição de tema.  <br/> |
|"LineGradientEnabled"  <br/> |Recupera o valor da célula LineGradientEnabled da definição de tema.  <br/> |
|"LineGradientDir"  <br/> |Recupera o valor da célula LineGradientDir da definição de tema.  <br/> |
|"LineGradientAngle"  <br/> |Recupera o valor da célula LineGradientAngle da definição de tema.  <br/> |
|"FillGradientEnabled"  <br/> |Recupera o valor da célula FillGradientEnabled da definição de tema.  <br/> |
|"FillGradientDir"  <br/> |Recupera o valor da célula FillGradientDir da definição de tema.  <br/> |
|"FillGradientAngle"  <br/> |Recupera o valor da célula FillGradientAngle da definição de tema.  <br/> |
|"RotateGradientWithShape"  <br/> |Recupera o valor da célula RotateGradientWithShape da definição de tema.  <br/> |
|"UseGroupGradient"  <br/> |Recupera o valor da célula UseGroupGradient da definição de tema.  <br/> |
|"ShadowType"  <br/> |Recupera o valor da célula ShapeShdwType da definição de tema.  <br/> |
|"ShadowColor"  <br/> |Recupera o valor da célula ShdwColor da definição de tema.  <br/> |
|"ShadowTransparency"  <br/> |Recupera o valor da célula ShdwColorTrans da definição de tema.  <br/> |
|"ShadowMagnification"  <br/> |Recupera o valor da célula ShapeShdwScaleFactor da definição de tema.  <br/> |
|"ShadowBlur"  <br/> |Recupera o valor da célula ShapeShdwBlur da definição de tema.  <br/> |
|"ShadowXOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetX da definição de tema.  <br/> |
|"ShadowYOffset"  <br/> |Recupera o valor da célula ShapeShdwOffsetY da definição de tema.  <br/> |
|"ShadowDirection"  <br/> |Recupera o valor da célula ShapeShdwObliqueAngle da definição de tema.  <br/> |
|"ShadowPattern"  <br/> |Recupera o valor da célula ShdwPattern da definição de tema.  <br/> |
|"BevelTopType"  <br/> |Recupera o valor da célula BevelTopType da definição de tema.  <br/> |
|"BevelTopWidth"  <br/> |Recupera o valor da célula BevelTopWidth da definição de tema.  <br/> |
|"BevelTopHeight"  <br/> |Recupera o valor da célula BevelTopHeight da definição de tema.  <br/> |
|"BevelMaterial"  <br/> |Recupera o valor da célula BevelMaterialType da definição de tema.  <br/> |
|"BevelLighting"  <br/> |Recupera o valor da célula BevelLightingType da definição de tema.  <br/> |
|"BevelLightingAngle"  <br/> |Recupera o valor da célula BevelLightingAngle da definição de tema.  <br/> |
|"BevelContourColor"  <br/> |Recupera o valor da célula BevelContourColor da definição de tema.  <br/> |
|"BevelContourSize"  <br/> |Recupera o valor da célula BevelContourSize da definição de tema.  <br/> |
|"ReflectionBlur"  <br/> |Recupera o valor da célula ReflectionBlur da definição de tema.  <br/> |
|"ReflectionDist"  <br/> |Recupera o valor da célula ReflectionDist da definição de tema.  <br/> |
|"ReflectionSize"  <br/> |Recupera o valor da célula ReflectionSize da definição de tema.  <br/> |
|"ReflectionTrans"  <br/> |Recupera o valor da célula ReflectionTrans da definição de tema.  <br/> |
|"SoftEdgesSize"  <br/> |Recupera o valor da célula SoftEdgesSize da definição de tema.  <br/> |
|"GlowSize"  <br/> |Recupera o valor da célula GlowSize da definição de tema.  <br/> |
|"GlowColor"  <br/> |Recupera o valor da célula GlowColor da definição de tema.  <br/> |
|"GlowTransparency"  <br/> |Recupera o valor da célula GlowColorTrans da definição de tema.  <br/> |
|"SketchAmount"  <br/> |Recupera o valor da célula SketchAmount da definição de tema.  <br/> |
|"SketchEnabled"  <br/> |Recupera o valor da célula SketchEnabled da definição de tema.  <br/> |
|"SketchFillChange"  <br/> |Recupera o valor da célula SketchFillChange da definição de tema.  <br/> |
|"SketchLineChange"  <br/> |Recupera o valor da célula SketchLineChange da definição de tema.  <br/> |
|"SketchLineWeight"  <br/> |Recupera o valor da célula SketchLineWeight da definição de tema.  <br/> |
|"LatinFont"  <br/> |Recupera o valor da célula fonte da definição de tema.  <br/> |
|"TextColor"  <br/> |Recupera o valor da célula de cor da definição de tema.  <br/> |
|"TextStyle"  <br/> |Recupera o valor da célula Character.Style da definição de tema.  <br/> |
|"ComplexFont"  <br/> |Recupera o valor da célula ComplexScriptFont da definição de tema.  <br/> |
|"AsianFont"  <br/> |Recupera o valor da célula AsianFont da definição de tema.  <br/> |
|"Color FillStop [x]"  <br/> |Recupera o valor da célula Color na linha *x* da definição de tema.  <br/> |
|"Transparência FillStop [x]"  <br/> |Recupera o valor da célula ColorTrans na linha *x* da definição de tema.  <br/> |
|"Posição FillStop [x]"  <br/> |Recupera o valor da célula posição na linha *x* da definição de tema.  <br/> |
|"Color LineStop [x]"  <br/> |Recupera o valor da célula Color na linha *x* da definição de tema.  <br/> |
|"Transparência LineStop [x]"  <br/> |Recupera o valor da célula ColorTrans na linha *x* da definição de tema.  <br/> |
|"Posição LineStop [x]"  <br/> |Recupera o valor da célula posição na linha *x* da definição de tema.  <br/> |
   
## <a name="example"></a>Exemplo

 `THEMEVAL("5")`
  
Retorna a cor de "Ênfase 3" da definição de tema.
  
 `THEMEVAL("LineWeight", "0.7 pt.")`
  
Retorna o valor da célula "LineWeight" da definição de tema. Se a forma que contém essa função não tiver nenhum tema aplicado a ela, a função retornará 'pt 0,7.'.
  

