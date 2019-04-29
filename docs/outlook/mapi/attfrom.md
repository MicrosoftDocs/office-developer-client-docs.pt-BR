---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432412"
---
# <a name="attfrom"></a>attFrom

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attFrom** é codificado como uma estrutura **TRP** que codifica o nome de exibição e o endereço de email do remetente, seguido do nome para exibição e do endereço do remetente, seguido de qualquer preenchimento necessário. O formato de **attFrom** é o seguinte: 
  
**attFrom**: _TRP-Structure_ Sender-display-name _ Sender-address _ Padding 
    
O Sender-Display-Name é uma cadeia de caracteres terminada em nulo que é preenchida com um caractere nulo adicional, se necessário, para atingir um limite de 2 bytes. O preenchimento no final da codificação **attFrom** consiste em quantos caracteres nulos forem necessários para atingir um limite de **sizeof (TRP)** . 
  
_TRP-estrutura:_ **trpidOneOff** cbgrtrp cch CB 
    
Para o item **attFrom** , o **TRP**-Structure sempre é uma codificação única, portanto, o trpid do campo **TRP**-Structure sempre é **trpidOneOff**. Os itens cbgrtrp, cch e CB correspondem aos campos restantes da estrutura **TRP** . 
  
O campo cbgrtrp é calculado como a soma de **(sizeof (TRP) \*2)**, o comprimento do remetente-display-display-NULL termina com seu enchimento e o comprimento do endereço de remetentes terminada em nulo.
  
O campo cch é calculado como o comprimento do nome de exibição terminada por caractere nulo com seu preenchimento.
  
O campo CB é calculado como o comprimento do endereço de remetentes terminada em nulo.
  
_remetente-endereço:_ tipo de endereço **:** endereço **' \ 0 '**
    
O endereço do remetente é uma cadeia de caracteres que é composta de quatro partes, o tipo de endereço, um caractere de dois-pontos literal (:), o próprio endereço e um caractere nulo de terminação. Por exemplo, a cadeia `fax:1-909-555-1234\0` de caracteres seria um valor de endereço de remetente legal.
  

