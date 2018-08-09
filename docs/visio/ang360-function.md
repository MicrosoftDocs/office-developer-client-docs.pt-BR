---
title: Função ANG360
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normaliza o intervalo de um ângulo.
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771259"
---
# <a name="ang360-function"></a>Função ANG360

Normaliza o intervalo de um ângulo para ser 0 \<= resultado \< 2PI radianos (0 \<= resultado \< 360 graus).
  
## <a name="syntax"></a>Sintaxe

ANG360 (* * *ângulo* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ângulo_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O ângulo a ser normalizado.  <br/> |
   
## <a name="remarks"></a>Comentários

Se o *ângulo* não for especificado, usando as unidades angulares, ela será interpretada como radianos. Se o *ângulo* não puder ser convertida para um valor, um #VALUE! erro será retornado. 
  
## <a name="example-1"></a>Exemplo 1

ANG360(395 graus)
  
Retorna 35 graus
  
## <a name="example-2"></a>Exemplo 2

ANG360(-9,8 rad)
  
Retorna 2,7664 rad.
  
## <a name="example-3"></a>Exemplo 3

ANG360(45)
  
Retorna 58,31 graus (1,0177 rad).
  

