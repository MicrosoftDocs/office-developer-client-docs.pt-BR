---
title: Função RECTSECT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcula o setor de um retângulo associado a x e y e retorna um inteiro de 0 a 4, indicando o setor.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160269"
---
# <a name="rectsect-function"></a>Função RECTSECT

Calcula o setor de um retângulo associado a  *x*  e  *y*  e retorna um inteiro de 0 a 4, indicando o setor. 
  
## <a name="syntax"></a>Sintaxe

RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obrigatório  <br/> |**String** <br/> |Largura do retângulo.  <br/> |
| _height_ <br/> |Obrigatório  <br/> |**String** <br/> |Altura do retângulo.  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada x.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada y.  <br/> |
| _option_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como os pontos colocados nas diagonais são tratados. Configure o valor como 0 para usar os setores esquerdo e direito para os pontos em uma diagonal. Configure o valor como 1 para usar os setores superior e inferior para os pontos em uma diagonal.  <br/> |
   
## <a name="remarks"></a>Comentários

Considere um retângulo que tenha uma  *largura*  e  *uma altura*  e um ponto (*x,y*) do ponto central do retângulo. Trace linhas diagonais nos cantos do retângulo para dividi-lo em quatro setores e um ponto central. Os setores de 0 a 4 representam o ponto central, direito, superior, esquerdo e inferior respectivamente. 
  
![Setores 0 a 4 representam o ponto central, direito, superior, esquerdo e inferior, respectivamente](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Exemplo

RECTSECT(1 pol, 2 pol, 1 pol, -7 pol, 0) 
  
Retornará 4. 
  

