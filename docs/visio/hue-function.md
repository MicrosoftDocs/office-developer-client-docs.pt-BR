---
title: Função HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Retorna o valor do componente de matiz de uma cor.
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772034"
---
# <a name="hue-function"></a>Função HUE

Retorna o valor do componente de matiz de uma cor.
  
## <a name="syntax"></a>Sintaxe

MATIZ (* * *expressão* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma expressão que é avaliada para uma cor.  <br/> |
   
### <a name="return-value"></a>Valor retornado

Number
  
## <a name="remarks"></a>Comentários

O valor retornado é um número entre 0 e 239, inclusive. A entrada é um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores. A função retornará 0 para uma entrada inválida. 
  
## <a name="example-1"></a>Exemplo 1

MATIZ (Sheet.4! FillForegnd)
  
Retornará a matiz da cor de preenchimento de primeiro plano de Sheet.4.
  
## <a name="example-2"></a>Exemplo 2

HUE(7)
  
Retornará 120 se o documento utilizar a paleta de cores padrão do Microsoft Visio, sendo ciano a cor do índice 7.
  
## <a name="example-3"></a>Exemplo 3

HUE(HSL(10, 20, 30) )
  
Retornará 10.
  

