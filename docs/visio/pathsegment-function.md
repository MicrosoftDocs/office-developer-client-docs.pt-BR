---
title: Função PATHSEGMENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: Retorna o número de segmento baseado em 1 na marca de percentual especificado no caminho especificado.
ms.openlocfilehash: b25f43ffa3c719cfc5ffbd1e417f2da9640e483b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772478"
---
# <a name="pathsegment-function"></a>Função PATHSEGMENT

Retorna o número de segmento baseado em 1 na marca de percentual especificado no caminho especificado.
  
## <a name="syntax"></a>Sintaxe

PATHSEGMENT (* * *seção* * *, * * *de viagem* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _viagem_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual do caminho percorrido, do ponto inicial ao ponto final. Deve estar entre 0 e 1.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  

