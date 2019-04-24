---
title: Função NOW (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Retorna o valor atual de data e hora.
ms.openlocfilehash: 9e28f51b0e1d1c09a70e54e432a865968c721940
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340989"
---
# <a name="now-function-visioshapesheet"></a>Função NOW (VisioShapeSheet)

Retorna o valor atual de data e hora.
  
## <a name="syntax"></a>Sintaxe

NOW ( )
  
### <a name="return-value"></a>Valor de retorno

DateTime
  
## <a name="remarks"></a>Comentários

NOW é recalculado automaticamente a cada minuto. 
  
## <a name="example-1"></a>Exemplo 1

NOW( )
  
Retornará a data e hora atuais, como 27/09/10 12:03:30.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(NOW(),"dd MMM., aaaa hh:mm")
  
Retornará a data e a hora atuais formatadas como 27 de setembro de 2010 12:03.
  
## <a name="example-3"></a>Exemplo 3

NOW () + 2EW.
  
Retornará a data e a hora atuais, além de duas semanas decorridas, como 11/10/10 12:03:30.
  

