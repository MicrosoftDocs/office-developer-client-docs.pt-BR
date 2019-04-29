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
description: Usado no parâmetro def_expressão da função SETATREF para indicar que def_expressão deve ser avaliada antes de atribuir ao parâmetro Reference em SETATREF.
ms.openlocfilehash: a11a7485e04d4deb31e9497476bb198d675bc68f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432979"
---
# <a name="setatrefeval-function"></a>Função SETATREFEVAL

Usado no parâmetro _def_expressão_ da função SETATREF para indicar que _def_expressão_ deve ser avaliada antes de atribuir ao parâmetro _Reference_ em SETATREF. 
  
## <a name="syntax"></a>Sintaxe

SETATREFEVAL (* * *expr* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expr_ <br/> |Obrigatório  <br/> |**Vai** <br/> | Uma expressão que é avaliada quando a função SETATREF redireciona _def_expressão_ para outra célula.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o parâmetro *def_expressão* da função SETATREF é atribuído a uma célula referenciada, o Microsoft Visio grava *def_expressão* na célula como uma expressão por padrão. No enTanto, se qualquer parte do parâmetro *def_expressão* for empacotada pela função SETATREFEVAL, o Visio avaliará a expressão e substituirá a função SETATREFEVAL com o seu resultado antes de resolver a expressão SETATREF. 
  
## <a name="example"></a>Exemplo

Para ver um exemplo, consulte a função [SETATREF](setatref-function.md). 
  

