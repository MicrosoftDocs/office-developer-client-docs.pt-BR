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
description: Avalia uma das duas expressões dependendo do valor do estado.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420343"
---
# <a name="userui-function"></a>Função USERUI

Avalia uma das duas expressões dependendo do valor de _estado._
  
## <a name="syntax"></a>Sintaxe

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Obrigatório  <br/> |**Boolean** <br/> |Determina qual expressão deve ser avaliada.  <br/> |
| _defaultexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |A expressão padrão.  <br/> |
| _userexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma expressão fornecida pelo usuário.  <br/> |
   
## <a name="remarks"></a>Comentários

Se  _o_ estado for 0, a função USERUI avaliará a  _expressão padrão_. Se _o_ estado for 1, avalia a _expressão do usuário._
  
## <a name="example"></a>Exemplo

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0,75) 
  
Avalia a expressão Width \* 0,075 e retorna o resultado. 
  

