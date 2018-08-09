---
title: Função MSOTINT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: Modifica a cor aumentando a luminosidade pelo percentual especificado.
ms.openlocfilehash: 50e81b5202174c61905d3914c50feddcb05a91cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772432"
---
# <a name="msotint-function"></a>Função MSOTINT

Modifica a cor aumentando a luminosidade pelo percentual especificado.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

MSOTINT (* * *cor* * *, * * *deltaLum* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**RGB** <br/> |O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.  <br/> |
| _deltaLum_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A alteração percentual entre branco (-100%) ou preto (100%) no valor _color_ .  <br/> |
   
## <a name="remarks"></a>Comentários

Quanto mais perto o valor _color_ estiver de branco ou preto, menor será a alteração na tonalidade produzida por um valor específico _deltaLum_ . 
  

