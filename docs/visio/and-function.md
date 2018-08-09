---
title: Função AND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251391
localization_priority: Normal
ms.assetid: 434d7ceb-1050-c667-fb3d-b6634440c18e
description: Retorna verdadeiro (1) se todas as expressões lógicas fornecidas forem TRUE. Se qualquer uma das expressões lógicas for FALSE ou 0, a função AND retorna FALSE (0).
ms.openlocfilehash: 27b2ef97ef1d0afde37596b18674c6de26355a1b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771278"
---
# <a name="and-function"></a>Função E

Retorna verdadeiro (1) se todas as expressões lógicas fornecidas forem TRUE. Se qualquer uma das expressões lógicas for FALSE ou 0, a função AND retorna FALSE (0).
  
## <a name="syntax"></a>Sintaxe

E (* * *expression1 lógica* * *, * * *expression2 lógica* * *,..., * * *lógicaN* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão lógica_ <br/> |Obrigatório  <br/> |**String** <br/> | Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor. Qualquer expressão avaliada como um valor diferente de zero é considerada VERDADEIRO.  <br/> |
   
## <a name="example"></a>Exemplo

E (altura \> 1, PinX \> 1)
  
Retorna VERDADEIRO se ambas as expressões forem VERDADEIRO. Se uma das expressões for FALSO, será retornado FALSO.
  

