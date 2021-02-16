---
title: Função BITAND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Retorna um número binário de 16 bits no qual cada bit é definido como 1 somente se o bit correspondente em binarynumber1 e binarynumber2 for 1. Caso contrário, o bit será definido como 0.
ms.openlocfilehash: a3c76a9122d0f02d5ab61460cf3457bb15da4d7b
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293489"
---
# <a name="bitand-function"></a>Função BITAND

Retorna um número binário de 16 bits no qual cada bit é definido como 1 somente se o bit correspondente em binarynumber1 e binarynumber2 for 1. Caso contrário, o bit será definido como 0. 
  
## <a name="syntax"></a>Sintaxe

BITAND(***binarynumber1***, ***binarynumber2*** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _binary number1_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O primeiro número binário de 16 bits.  <br/> |
| _binary number2_ <br/> |Obrigatório  <br/> |**Numérica** <br/> |O segundo número binário de 16 bits.  <br/> |
   
## <a name="remarks"></a>Comentários

É possível usar esta função para testar e alterar propriedades de uma forma armazenadas como bitmasks, por exemplo, o formato do texto da célula.
  
## <a name="example"></a>Exemplo

BITAND(12,6)
  
Retornará 4. Se 12 = 0...01100 e 6 = 0...00110; consequentemente, BITAND(12,6) = 0...00100.
  

