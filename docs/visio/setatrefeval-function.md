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
description: Usado no parâmetro set_expression da função SETATREF para indicar que set_expression deve ser avaliado antes de atribuir ao parâmetro de referência em SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432979"
---
# <a name="setatrefeval-function"></a>Função SETATREFEVAL

Usado no parâmetro _set_expression_ da função SETATREF para  indicar que set_expression deve ser avaliado  antes de atribuir ao parâmetro de referência em SETATREF. 
  
## <a name="syntax"></a>Sintaxe

SETATREFEVAL(** *expr* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obrigatório  <br/> |**Varia** <br/> | Uma expressão avaliada quando a função SETATREF redireciona set_expression  _para_ outra célula.  <br/> |
   
## <a name="remarks"></a>Comentários

Ao atribuir o *set_expression* parâmetro da função SETATREF a uma célula referenciada, o Microsoft Visio grava set_expression na célula como uma expressão por padrão.  No entanto, se qualquer parte do parâmetro set_expression for envolvida pela função SETATREFEVAL, o Visio avaliará a expressão e substituirá  *a*  função SETATREFEVAL pelo resultado antes de resolver a expressão SETATREF. 
  
## <a name="example"></a>Exemplo

Para ver um exemplo, consulte a função [SETATREF](setatref-function.md). 
  

