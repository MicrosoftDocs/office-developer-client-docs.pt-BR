---
title: Função PNT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: Retorna o ponto representado pelas coordenadas x e y como um único valor.
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772557"
---
# <a name="pnt-function"></a>Função PNT

Retorna o ponto representado pelas coordenadas _x_ e _y_ como um único valor. 
  
## <a name="syntax"></a>Sintaxe

PNT (* * *x, y* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |Obrigatório  <br/> |**Número, Número** <br/> |As coordenadas do ponto do sistema de coordenadas da forma atual.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Ponto
  
## <a name="remarks"></a>Comentários

Convertendo coordenadas para pontos permite alterar a geometria de uma forma sem precisar manipular *x* e *y* -coordena separadamente. 
  
## <a name="example"></a>Exemplo

PNT(PinX,PinY) 
  
Retornará o ponto representado por PinX e PinY. 
  

