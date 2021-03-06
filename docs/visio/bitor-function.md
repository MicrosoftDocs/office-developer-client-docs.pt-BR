---
title: Função BITOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente no número binário1 ou no número binário2 for 1. O bit é definido como 0 somente se o bit correspondente for 0 no número binário1 e no número binário2 .
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408079"
---
# <a name="bitor-function"></a>Função BITOR

Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente no número  *binário1*  ou no número  *binário2*  for 1. O bit é definido como 0 somente se o bit correspondente for 0 no número  *binário1*  e  *no número binário2*  . 
  
## <a name="syntax"></a>Sintaxe

BITOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binary number2_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITOR(12,6)
  
Retornará 14. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITOR(12,6) = 0...01110.
  

