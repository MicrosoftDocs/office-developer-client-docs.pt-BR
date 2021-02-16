---
title: Função GETREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é mudada.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424326"
---
# <a name="getref-function"></a>Função GETREF

Faz referência a uma célula e não recalcula a fórmula quando a célula referenciada é mudada.
  
## <a name="syntax"></a>Sintaxe

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Obrigatório  <br/> |**String** <br/> |O nome da célula a ser referenciada.  <br/> |
   
## <a name="example"></a>Exemplo

SETF(GETREF(PinX),5.1) 
  
Define a fórmula da célula PinX para 5,1. 
  

