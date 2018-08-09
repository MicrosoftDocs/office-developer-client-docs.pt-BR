---
title: Função PAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Retorna a coordenada x, y de um ponto no sistema de coordenadas do pai da forma.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772467"
---
# <a name="par-function"></a>Função PAR

Retorna as coordenadas _x, y_ de um ponto no sistema de coordenadas do pai da forma. 
  
## <a name="syntax"></a>Sintaxe

PAR (* * *aponte* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ponto_ <br/> |Obrigatório  <br/> |**Número, Número** <br/> |As coordenadas do ponto do sistema de coordenadas da forma atual.  <br/> |
   
## <a name="remarks"></a>Comentários

No Microsoft Visio, um ponto é um valor único que incorpora um par de *x* e *y* -coordenadas. Se a forma estiver em um grupo, seu pai é o grupo. Se a forma não estiver em um grupo, seu pai é a página. 
  
## <a name="example"></a>Exemplo

PAR(PNT(PinX,PinY)) 
  
Nesta expressão, PNT converte um par de coordenadas na forma atual em um ponto. Em seguida, PAR converte o ponto em um par de coordenadas em relação ao canto inferior esquerdo da página ou do grupo que contém a forma atual. 
  

