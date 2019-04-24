---
title: Função PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Retorna o número de segmento baseado em 1 na marca de porcentagem especificada ao longo do caminho especificado.
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344447"
---
# <a name="pathsegment-function"></a>Função PATHSEGMENT

Retorna o número de segmento baseado em 1 na marca de porcentagem especificada ao longo do caminho especificado.
  
## <a name="syntax"></a>Sintaxe

PATHSEGMENT (* * *seção* * *, * * *viagem* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _transmiti_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual do caminho percorrido, do ponto inicial ao ponto final. Deve estar entre 0 e 1.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Integer
  

