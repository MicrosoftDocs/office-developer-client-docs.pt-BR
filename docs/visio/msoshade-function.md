---
title: Função MSOSHADE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: Modifica a cor reduzindo a luminosidade pelo percentual especificado.
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283707"
---
# <a name="msoshade-function"></a>Função MSOSHADE

Modifica a cor reduzindo a luminosidade pelo percentual especificado.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

MSOSHADE (* * *cor* * *, * * *-deltaLum* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |Obrigatório  <br/> |**RGB** <br/> |O valor de cor RGB (vermelho, verde, azul) padrão ou a referência a uma cor.  <br/> |
| _-deltaLum_ <br/> |Obrigatório  <br/> |**Integer** <br/> |A alteração percentual em direção ao branco (-100%) ou preto (100%) do valor de _cor_ .  <br/> |
   
## <a name="remarks"></a>Comentários

Quanto mais próximo o valor de _cor_ for branco ou preto, menor será a alteração na sombra produzida por um valor _deltaLum_ específico. 
  

