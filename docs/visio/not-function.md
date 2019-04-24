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
description: Retorna TRUE (1) se logicaly for FALSE. Caso contrário, retornará FALSE (0).
ms.openlocfilehash: 3359e21654bcc318caf31405093f851eca064119
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341124"
---
# <a name="not-function"></a>Função NOT

Retorna TRUE (1) se _logicaly_ for false. Caso contrário, retornará FALSE (0). 
  
## <a name="syntax"></a>Sintaxe

NOT (* * *logicalid* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Obrigatório  <br/> |**String** <br/> |A expressão lógica a ser avaliada.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Booliano
  
## <a name="example"></a>Exemplo

Não (altura \> de 0,75 in) 
  
Retorna 1 se a Altura for menor que ou igual a 0,75 polegadas. Retorna 0 se a Altura for maior que 0,75 polegadas. 
  

