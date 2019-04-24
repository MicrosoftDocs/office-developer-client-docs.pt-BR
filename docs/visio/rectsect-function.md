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
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360021"
---
# <a name="rectsect-function"></a>Função RECTSECT

Calcula o setor de um retângulo associado a *x* e *y* e retorna um inteiro de 0 a 4, indicando o setor. 
  
## <a name="syntax"></a>Sintaxe

RECTSECT (* * *largura* * *, * * *altura* * *, * * *x* * *, * * *y* * *, * * *opção* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |Obrigatório  <br/> |**String** <br/> |Largura do retângulo.  <br/> |
| _height_ <br/> |Obrigatório  <br/> |**String** <br/> |Altura do retângulo.  <br/> |
| _x_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada x.  <br/> |
| _y_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma coordenada y.  <br/> |
| _ValorDeOpção_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Especifica como os pontos colocados nas diagonais são tratados. Configure o valor como 0 para usar os setores esquerdo e direito para os pontos em uma diagonal. Configure o valor como 1 para usar os setores superior e inferior para os pontos em uma diagonal.  <br/> |
   
## <a name="remarks"></a>Comentários

Considere um retângulo com *largura* e *altura* , e um ponto (*x, y*) do ponto central do retângulo. Trace linhas diagonais nos cantos do retângulo para dividi-lo em quatro setores e um ponto central. Os setores de 0 a 4 representam o ponto central, direito, superior, esquerdo e inferior respectivamente. 
  
![Os setores 0 a 4 representam o ponto central, direito, superior, esquerdo e inferior, respectivamente](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>Exemplo

RECTSECT(1 pol, 2 pol, 1 pol, -7 pol, 0) 
  
Retornará 4. 
  

