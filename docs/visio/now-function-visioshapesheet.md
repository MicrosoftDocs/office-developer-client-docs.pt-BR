---
title: Agora a função (VisioShapeSheet)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251470
localization_priority: Normal
ms.assetid: 96cac1f6-cc17-466f-23d8-a9006e7de05f
description: Retorna o valor de data e hora atual.
ms.openlocfilehash: 387425369b1f1d6313502b3679a72cfd23038834
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772446"
---
# <a name="now-function-visioshapesheet"></a>Agora a função (VisioShapeSheet)

Retorna o valor de data e hora atual.
  
## <a name="syntax"></a>Sintaxe

NOW ( )
  
### <a name="return-value"></a>Valor retornado

Datetime
  
## <a name="remarks"></a>Comentários

NOW é recalculado automaticamente a cada minuto. 
  
## <a name="example-1"></a>Exemplo 1

NOW( )
  
Retornará a data e hora atuais, como 27/09/10 12:03:30.
  
## <a name="example-2"></a>Exemplo 2

FORMAT(NOW(),"dd MMM., aaaa hh:mm")
  
Retornará a data e a hora atuais formatadas como 27 de setembro de 2010 12:03.
  
## <a name="example-3"></a>Exemplo 3

NOW()+2EW.
  
Retornará a data e a hora atuais, além de duas semanas decorridas, como 11/10/10 12:03:30.
  

