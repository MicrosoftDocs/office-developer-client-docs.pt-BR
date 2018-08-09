---
title: Função MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica a cor reduzindo a luminosidade pelo percentual especificado.
ms.openlocfilehash: f5f6eb0b6009473dcec017e951cca2f90b6c4d55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772403"
---
# <a name="msoshade-function"></a>Função MSOSHADE

Modifica a cor reduzindo a luminosidade pelo percentual especificado.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

MSOSHADE (* * *cor* * *, * * *- deltaLum* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**RGB** <br/> |O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.  <br/> |
| _-deltaLum_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A alteração percentual entre branco (-100%) ou preto (100%) no valor _color_ .  <br/> |
   
## <a name="remarks"></a>Comentários

Quanto mais perto o valor _color_ estiver de branco ou preto, menor será a alteração no sombreamento produzido por um valor específico _- deltaLum_ . 
  

