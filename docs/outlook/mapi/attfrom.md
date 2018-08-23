---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6460cd3ef0495a5494e03b4c7034e067cf8793b7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576061"
---
# <a name="attfrom"></a>attFrom

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attFrom** é codificado como uma estrutura **TRP** que codifica o exibição nome e endereço de email do remetente, seguido do nome para exibição e o endereço do remetente, seguido de qualquer preenchimento necessário. O formato **attFrom** é da seguinte maneira: 
  
**attFrom**: preenchimento de _ _TRP-estrutura_ _ do nome de exibição do remetente endereço do remetente 
    
O remetente-exibição-name é uma cadeia de caracteres terminada em nulo que é preenchida com um caractere nulo adicional, se necessário, para atingir um limite de 2 bytes. O preenchimento no final da codificação **attFrom** consiste em quantos caracteres nulos conforme necessário para alcançar um limite de **sizeof(TRP)** . 
  
_Estrutura de TRP:_ **trpidOneOff** cbgrtrp cch cb 
    
Para o item **attFrom** , o **TRP**-estrutura é sempre um únicos encoding, portanto o trpid desativa o **TRP**-campo estrutura é sempre **trpidOneOff**. Os itens de cb, cch e cbgrtrp correspondem aos campos restantes da estrutura **TRP** . 
  
O campo cbgrtrp é calculado como a soma de **(sizeof(TRP) \*2)**, o comprimento do terminada em nulo remetente--nome para exibição com seu preenchimento e o comprimento do endereço de remetente terminada em nulo.
  
O campo cch é calculado como o comprimento do terminada em nulo-nome para exibição com seu preenchimento.
  
O campo cb é calculado como o comprimento do endereço de remetente terminada em nulo.
  
_endereço do remetente:_ **:** de tipo de endereço **'\0'** de endereços
    
O endereço do remetente é uma cadeia de caracteres que é composta de quatro partes, o tipo de endereço, dois pontos literal (:), o próprio endereço e um caractere nulo de terminação. Por exemplo, a cadeia de caracteres `fax:1-909-555-1234\0` seria um valor de endereço de remetente legal.
  

