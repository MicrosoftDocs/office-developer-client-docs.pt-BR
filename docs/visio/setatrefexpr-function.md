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
description: Armazena um valor definido por meio de uma ação na interface do usuário ou automação.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439048"
---
# <a name="setatrefexpr-function"></a>Função SETATREFEXPR

Armazena um valor definido por meio de uma ação na interface do usuário ou automação.
  
## <a name="syntax"></a>Sintaxe

SETATREFEXPR ([* * *expr_opt* * *]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expr_opt_ <br/> |Opcional  <br/> |**Vai** <br/> |Uma expressão substituída pelo valor ou expressão atribuída à célula referenciada na função SETATREF. Se não for indicado, seu valor inicial será 0 (zero).  <br/> |
   
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
  
PinX = INT (SETATREFEXPR ()/User.GridX + 0,5)\*User. gradex
  
PinY = INT (SETATREFEXPR ()/User.GridY + 0,5)\*User. GridY
  
## <a name="example-3"></a>Exemplo 3

Para um exemplo usando a função SETATREFEXPR com a função SETATREF, consulte a função [SETATREF](setatref-function.md). 
  

