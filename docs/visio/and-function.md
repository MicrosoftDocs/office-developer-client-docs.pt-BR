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
description: Retorna TRUE (1) se todas as expressões lógicas fornecidas são TRUE. Se qualquer uma das expressões lógicas for FALSE ou 0, a função e retornará FALSE (0).
ms.openlocfilehash: 74e8301718e69a2ab61f6bf9992d0d6855bbc6f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422009"
---
# <a name="and-function"></a>Função E

Retorna TRUE (1) se todas as expressões lógicas fornecidas são TRUE. Se qualquer uma das expressões lógicas for FALSE ou 0, a função e retornará FALSE (0).
  
## <a name="syntax"></a>Sintaxe

AND (* * *logical expression1* * *, * * *logical expression2* * *,..., * * *expressão lógican* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expressão lógica_ <br/> |Obrigatório  <br/> |**Cadeia de caracteres** <br/> | Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor. Qualquer expressão avaliada como um valor diferente de zero é considerada VERDADEIRO.  <br/> |
   
## <a name="example"></a>Exemplo

E (altura \> 1, PinX \> 1)
  
Retorna VERDADEIRO se ambas as expressões forem VERDADEIRO. Se uma das expressões for FALSO, será retornado FALSO.
  

