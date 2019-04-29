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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417193"
---
# <a name="ang360-function"></a>Função ANG360

Normaliza o intervalo de um ângulo para ser 0 \<= resultado \< 2PI radianos (0 \<= resultado \< 360 graus).
  
## <a name="syntax"></a>Sintaxe

ANG360 (* * *Angle* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ângulo_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O ângulo a ser normalizado.  <br/> |
   
## <a name="remarks"></a>Comentários

Se *Angle* não for especificado usando unidades angulares, será interpretado como radianos. Se o *ângulo* não puder ser convertido em um valor, um #VALUE! será retornado. 
  
## <a name="example-1"></a>Exemplo 1

ANG360(395 graus)
  
Retorna 35 graus
  
## <a name="example-2"></a>Exemplo 2

ANG360(-9,8 rad)
  
Retorna 2,7664 rad.
  
## <a name="example-3"></a>Exemplo 3

ANG360 (45)
  
Retorna 58,31 graus (1,0177 rad).
  

