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
description: Avalia uma das duas expressões dependendo do valor de State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420343"
---
# <a name="userui-function"></a>Função USERUI

Avalia uma das duas expressões dependendo do valor de _State_.
  
## <a name="syntax"></a>Sintaxe

USERUI (* * *estado* * *, * * *DefaultName* * *, * * *username* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Determina a expressão a ser avaliada.  <br/> |
| _DefaultName_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |A expressão padrão.  <br/> |
| _username_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> |Uma expressão fornecida pelo usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Se _State_ for 0, a função USERUI avaliará o _DefaultName_. Se _State_ for 1, ele avaliará a _username_.
  
## <a name="example"></a>Exemplo

USERUI (1, se (Width\>6pol, 6Pol, Width), Width\*0,75) 
  
Avalia a expressão largura\*. 075 e retorna o resultado. 
  

