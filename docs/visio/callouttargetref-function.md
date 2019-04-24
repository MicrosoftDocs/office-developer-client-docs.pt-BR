---
title: Função CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337244"
---
# <a name="callouttargetref-function"></a>Função CALLOUTTARGETREF

Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
  
## <a name="version-information"></a>Informações da versão

Version Added: Visio 2010
 
  
## <a name="syntax"></a>Sintaxe

CALLOUTTARGETREF ()!
  
### <a name="return-value"></a>Valor de retorno

Referência do ShapeSheet
  
## <a name="remarks"></a>Comentários

Se a forma não for uma forma de texto explicativo ou não estiver associada a uma forma de destino, CALLOUTTARGETREF retornará #REF.
  
## <a name="example"></a>Exemplo

CALLOUTTARGETREF ()! Height 
  
Retorna o valor na célula Height da forma associada ao texto explicativo. 
  

