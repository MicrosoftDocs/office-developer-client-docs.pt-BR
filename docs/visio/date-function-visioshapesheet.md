---
title: Função DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Retorna a data representada por dia, mês e ano formatada de acordo com o estilo de data curta em configurações regionais do sistema. Os valores para o ano, mês e dia refletem o calendário gregoriano.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771681"
---
# <a name="date-function-visioshapesheet"></a>Função DATE (VisioShapeSheet)

Retorna a data representada por *ano, mês,* *dia* e formatada de acordo com o estilo de data curta em configurações regionais do sistema. Os valores para o *ano*, *mês* e *dia* refletem o calendário gregoriano. 
  
## <a name="syntax"></a>Sintaxe

Data (* * *ano* * *, * * *mês* * *, * * *dia* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _year_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O ano.  <br/> |
| _Mês_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O mês.  <br/> |
| _day_ <br/> |Obrigatório  <br/> |**Integer** <br/> |O dia.  <br/> |
   
## <a name="example-1"></a>Exemplo 1

DATE(1999,6,7)
  
Retornará o valor que representa 07/06/1999.
  
## <a name="example-2"></a>Exemplo 2

DATE(1999,6,7) + 4 ed.
  
Retornará o valor que representa 11/06/99.
  
## <a name="example-3"></a>Exemplo 3

FORMAT(DATE(1999,10,14),"C")
  
Retornará o valor que representa terça-feira, 14 de outubro de 1999.
  

