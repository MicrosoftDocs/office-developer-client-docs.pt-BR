---
title: Função NOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251469
localization_priority: Normal
ms.assetid: 65873b32-2406-7c33-8e68-802461f467b2
description: Retorna VERDADEIRO (1) se expressão lógica for FALSO. Caso contrário, retornará FALSO (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413329"
---
# <a name="not-function"></a>Função NOT

Retorna VERDADEIRO (1) se  _expressão lógica for_ FALSO. Caso contrário, retornará FALSO (0). 
  
## <a name="syntax"></a>Sintaxe

NOT(** *logicalexpression* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |A expressão lógica a ser avaliada.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="example"></a>Exemplo

NOT(Height \> 0,75 in) 
  
Retorna 1 se a Altura for menor que ou igual a 0,75 polegadas. Retorna 0 se a Altura for maior que 0,75 polegadas. 
  

