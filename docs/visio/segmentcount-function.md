---
title: Função SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Retorna o número de segmentos de linha que formam o caminho.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326037"
---
# <a name="segmentcount-function"></a>Função SEGMENTCOUNT

Retorna o número de segmentos de linha que formam o caminho.
  
## <a name="syntax"></a>Sintaxe

SEGMENTCOUNT (* * *pathRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à célula Path (por exemplo, Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Inteiro
  
## <a name="remarks"></a>Comentários

Saltos de linha não são incluídos no número total de segmentos retornados.
  

