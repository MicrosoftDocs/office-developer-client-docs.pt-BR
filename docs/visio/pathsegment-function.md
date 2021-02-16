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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432482"
---
# <a name="pathsegment-function"></a>Função PATHSEGMENT

Retorna o número de segmento baseado em 1 na marca de porcentagem especificada ao longo do caminho especificado.
  
## <a name="syntax"></a>Sintaxe

PATHSEGMENT(** *section* **, ** *travel* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Obrigatório  <br/> |**String** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à sua respectiva célula Path (por exemplo, Geometry1.Path).  <br/> |
| _travel_ <br/> |Obrigatório  <br/> |**Double** <br/> |O percentual do caminho percorrido, do ponto inicial ao ponto final. Deve estar entre 0 e 1.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  

