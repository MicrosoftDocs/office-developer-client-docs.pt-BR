---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567472"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attSentFor** é codificado como cadeias de caracteres contadas apresentados ponta a ponta. O formato **attSentFor** é da seguinte maneira: 
  
 **attSentFor**: 
  
> nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_
    
 _endereço de email_
  
> endereço do tipo **:** 
    
Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados. Eles ainda incluem abortar caracteres null, no entanto. As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com". Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.
  

