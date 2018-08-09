---
title: Função LUM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: Retorna o valor de componente de luminosidade de uma cor.
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772302"
---
# <a name="lum-function"></a>Função LUM

Retorna o valor de componente de luminosidade de uma cor.
  
## <a name="syntax"></a>Sintaxe

LUM (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**Numérico** <br/> |O índice de uma cor na tabela de cores do documento ou uma referência a uma célula que contenha um índice de cores.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

O valor retornado é um número no intervalo de 0 a 240, inclusive. A função retornará 0 para uma entrada inválida. 
  
## <a name="example-1"></a>Exemplo 1

LUM (Sheet.4! FillForegnd)
  
Retornará a luminosidade da cor de preenchimento de primeiro plano de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

LUM(6)
  
Retornará 120 se o documento utilizar a paleta de cores padrão do Visio, sendo magenta a cor do índice 6.
  
## <a name="example-3"></a>Exemplo 3

LUM(HSL(10, 20, 30))
  
Retornará 30.
  

