---
title: Função SETATREFEXPR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Armazena um valor que é definido por meio de uma ação na interface do usuário (UI) ou automação.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772880"
---
# <a name="setatrefexpr-function"></a>Função SETATREFEXPR

Armazena um valor que é definido por meio de uma ação na interface do usuário (UI) ou automação.
  
## <a name="syntax"></a>Sintaxe

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Opcional  <br/> |**Varia** <br/> |Uma expressão que é substituída pelo valor ou expressão que está sendo atribuído à célula referenciada na função SETATREF. Se não foi indicado, seu valor inicial é 0 (zero).  <br/> |
   
## <a name="remarks"></a>Comentários

O valor de uma expressão SETATREFEXPR também pode ser definido a partir de uma função SETATREF em outra célula que faça referência à célula que contém a expressão SETATREFEXPR. 
  
Você não está limitado a usar a função SETATREFEXPR como um parâmetro para a função SETATREF. 
  
## <a name="example-1"></a>Exemplo 1

O seguinte exemplo usa a função SETATREFEXPR para garantir que uma forma seja tão grande quanto seu texto.
  
Largura =MAX(TEXTWIDTH(TheText),SETATREFEXPR())
  
## <a name="example-2"></a>Exemplo 2

O seguinte exemplo mostra como você pode usar a função SETATREFEXPR para fazer com que sua forma se encaixe a uma grade personalizada. As fórmulas SETATREFEXPR são colocadas nas células PinX e PinY, fazendo com que o pino da forma se encaixe na grade definida em User.GridX e User.GridY. 
  
User.GridX =2 pol
  
User.GridY =2 pol
  
PinX = INT (SETATREFEXPR () /User.GridX +.5)\*User. GridX
  
PinY = INT (SETATREFEXPR () /User.GridY +.5)\*User. GridY
  
## <a name="example-3"></a>Exemplo 3

Para um exemplo usando a função SETATREFEXPR com a função SETATREF, consulte a função [SETATREF](setatref-function.md). 
  

