---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578035"
---
# <a name="attowner"></a>attOwner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attOwner** é codificado como cadeias de caracteres contadas apresentados ponta a ponta. O formato **attOwner** é da seguinte maneira: 
  
 **attOwner**: 
  
> nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_
    
 _endereço de email_
  
> endereço do tipo **:** 
    
Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados. Eles ainda incluem abortar caracteres null, no entanto. As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com". Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.
  
O mapeamento das propriedades MAPI para o atributo **attOwner** é dependente a classe de mensagem da mensagem que está sendo codificada. 
  

