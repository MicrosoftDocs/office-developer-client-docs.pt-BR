---
title: Função BITXOR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente em um deles, mas não o número binário1 e o número binário2 for 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439230"
---
# <a name="bitxor-function"></a>Função BITXOR

Retorna um número binário de 16 bits no qual cada bit é definido como 1 se o bit correspondente em um deles, mas não o número binário1 e o número binário2 for 1. Caso contrário, o bit será definido como 0.
  
## <a name="syntax"></a>Sintaxe

BITXOR(** *binary number1* **, ** *binary number2* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binary number2_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O segundo número binário de 16 bits.  <br/> |
   
### <a name="return-value"></a>Valor de retorno

Binário de 16 bits
  
## <a name="example"></a>Exemplo

BITXOR(12,6)
  
Retornará 10. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITXOR(12,6) = 0...01010.
  

