---
title: Função CALLOUTTARGETREF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771419"
---
# <a name="callouttargetref-function"></a>Função CALLOUTTARGETREF

Retorna uma referência de planilha para a forma de destino da forma de texto explicativo.
  
## <a name="version-information"></a>Informações da versão

Versão adicionada: Visio 2010 
  
## <a name="syntax"></a>Sintaxe

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>Valor retornado

Referência do ShapeSheet
  
## <a name="remarks"></a>Comentários

Se a forma não for uma forma de texto explicativo, ou se ele não estiver associado uma forma de destino, CALLOUTTARGETREF retornará #REF.
  
## <a name="example"></a>Example

CALLOUTTARGETREF()!Height 
  
Retorna o valor na célula Height da forma associada ao texto explicativo. 
  

