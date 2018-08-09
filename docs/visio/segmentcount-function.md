---
title: Função SEGMENTCOUNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Retorna o número de segmentos de linha que formam o caminho.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772868"
---
# <a name="segmentcount-function"></a>Função SEGMENTCOUNT

Retorna o número de segmentos de linha que formam o caminho.
  
## <a name="syntax"></a>Sintaxe

SEGMENTCOUNT (* * *pathRef* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _pathRef_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A seção Geometry que representa o caminho, especificada por uma referência à célula Path (por exemplo, Geometry1.Path).  <br/> |
   
### <a name="return-value"></a>Valor retornado

Inteiro
  
## <a name="remarks"></a>Comentários

Saltos de linha não são incluídos no número total de segmentos retornados.
  

