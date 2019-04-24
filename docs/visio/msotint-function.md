---
title: Função MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica a cor aumentando a luminosidade pelo percentual especificado.
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335193"
---
# <a name="msotint-function"></a>Função MSOTINT

Modifica a cor aumentando a luminosidade pelo percentual especificado.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

MSOTINT (* * *cor* * *, * * *deltaLum* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**RGB** <br/> |O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.  <br/> |
| _deltaLum_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A alteração percentual em direção ao branco (-100%) ou preto (100%) do valor de _cor_ .  <br/> |
   
## <a name="remarks"></a>Comentários

Quanto mais próximo o valor de _cor_ for branco ou preto, menor será a alteração na tonalidade produzida por um valor _deltaLum_ específico. 
  

