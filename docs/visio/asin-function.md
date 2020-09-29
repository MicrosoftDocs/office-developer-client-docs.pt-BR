---
title: Função ASIN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é núm.
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293503"
---
# <a name="asin-function"></a>Função ASIN

Retorna o arco seno de um número, por exemplo, o ângulo cujo seno é  *núm*  . 
  
## <a name="syntax"></a>Sintaxe

Asen (***número*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O seno do ângulo.  <br/> |
   
## <a name="remarks"></a>Comentários

O valor de entrada deve estar no intervalo-1 <=  *número*  <= 1, ou um #NUM! será retornado. O ângulo resultante está no intervalo-PI/2 <=  *angle*  <= pi/2 radianos (-90 <=  *angle*  <= 90 graus). 
  
## <a name="example"></a>Exemplo

ASEN (1)
  
Retorna 90 graus
  

