---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766231"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Aplica-se a**: Outlook 
  
O atributo **attSentFor** é codificado como cadeias de caracteres contadas apresentados ponta a ponta. O formato **attSentFor** é da seguinte maneira: 
  
 **attSentFor**: 
  
> nome para exibição do comprimento do nome de exibição endereço-comprimento _endereço de email_
    
 _endereço de email_
  
> endereço do tipo **:** 
    
Ao contrário de outro comprimento valores, o comprimento do nome de exibição e endereço comprimento são valores de 16 bits não assinados, em vez de inteiros longos não assinados. Eles ainda incluem abortar caracteres null, no entanto. As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos (:) literal, como "smtp:joe@nowhere.com". Somente a sequência de endereço do tipo combinada **:** é terminada em nulo.
  

