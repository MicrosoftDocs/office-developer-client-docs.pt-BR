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
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766211"
---
# <a name="attowner"></a>attOwner

  
  
**Aplica-se a**: Outlook 
  
O atributo **attOwner** é codificado como cadeias de caracteres contadas apresentados ponta a ponta. O formato **attOwner** é da seguinte maneira: 
  
 **attOwner**: 
  
> nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_
    
 _endereço de email_
  
> endereço do tipo **:** 
    
Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados. Eles ainda incluem abortar caracteres null, no entanto. As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com". Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.
  
O mapeamento das propriedades MAPI para o atributo **attOwner** é dependente a classe de mensagem da mensagem que está sendo codificada. 
  

