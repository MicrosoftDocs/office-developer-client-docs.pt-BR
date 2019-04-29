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
description: Retorna as coordenadas x, y de um ponto no sistema de coordenadas do pai da forma.
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414505"
---
# <a name="par-function"></a>Função PAR

Retorna as coordenadas _x, y_ de um ponto no sistema de coordenadas do pai da forma. 
  
## <a name="syntax"></a>Sintaxe

PAR (* * *ponto* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _ponto_ <br/> |Obrigatório  <br/> |**Número, Número** <br/> |As coordenadas do ponto do sistema de coordenadas da forma atual.  <br/> |
   
## <a name="remarks"></a>Comentários

No Microsoft Visio, um ponto é um valor único que incorpora um par de coordenadas *x* e *y* . Se a forma estiver em um grupo, seu pai será o grupo. Se não estiver em um grupo, seu pai será a página. 
  
## <a name="example"></a>Exemplo

PAR (PNT (PinX, PinY)) 
  
Nesta expressão, PNT converte um par de coordenadas na forma atual em um ponto. Em seguida, PAR converte o ponto em um par de coordenadas em relação ao canto inferior esquerdo da página ou do grupo que contém a forma atual. 
  

