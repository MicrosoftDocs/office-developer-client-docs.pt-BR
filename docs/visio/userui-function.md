---
title: Função USERUI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Avalia uma das duas expressões dependendo do valor de estado.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773238"
---
# <a name="userui-function"></a>Função USERUI

Avalia uma das duas expressões dependendo do valor de _estado_.
  
## <a name="syntax"></a>Sintaxe

USERUI (* * *estado* * *, * * *defaultexpression* * *, * * *userexpression* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Determina qual expressão a ser avaliada.  <br/> |
| _defaultexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |A expressão padrão.  <br/> |
| _userexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma expressão fornecida pelo usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o _estado_ for 0, a função USERUI avalia o _defaultexpression_. Se o _estado_ for 1, ela avalia o _userexpression_.
  
## <a name="example"></a>Exemplo

USERUI (1, se (largura\>6pol, 6pol, largura), largura\*0,75) 
  
Avalia a expressão largura\*.075 e retorna o resultado. 
  

