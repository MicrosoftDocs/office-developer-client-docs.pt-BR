---
title: Função SETATREFEVAL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1042150
localization_priority: Normal
ms.assetid: b3f3a0a0-7b14-0b71-d247-ada81b93b66b
description: Usado no parâmetro set_expression da função SETATREF para indicar que set_expression deve ser avaliada antes de atribuir ao parâmetro de referência em SETATREF.
ms.openlocfilehash: 0826ef9ca91e180576c0b2611452758b238736a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772858"
---
# <a name="setatrefeval-function"></a>Função SETATREFEVAL

Usado no parâmetro _set_expression_ da função SETATREF para indicar _set_expression_ deve ser avaliada antes de atribuir ao parâmetro de _referência_ em SETATREF. 
  
## <a name="syntax"></a>Sintaxe

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obrigatório  <br/> |**Varia** <br/> | Uma expressão que é avaliada quando a função SETATREF redireciona _set_expression_ para outra célula.  <br/> |
   
## <a name="remarks"></a>Comentários

Ao atribuir o parâmetro *set_expression* da função SETATREF a uma célula referenciada, o Microsoft Visio grava *set_expression* para a célula como uma expressão por padrão. No entanto, se qualquer parte do parâmetro *set_expression* é empacotado pela função SETATREFEVAL, o Visio avalia a expressão e substitui a função SETATREFEVAL pelo seu resultado antes de resolver a expressão SETATREF. 
  
## <a name="example"></a>Exemplo

Para ver um exemplo, consulte a função [SETATREF](setatref-function.md). 
  

