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
  
O atributo **attFrom** é codificado como uma estrutura **TRP** que codifica o nome para exibição e o endereço de email do remetente, seguido pelo nome de exibição e endereço do remetente, seguido por qualquer preenchimento necessário. O formato para **attFrom** é o seguinte: 
  
**attFrom**: _preenchimento TRP-structure_ sender-display-name _ sender-address _ 
    
O sender-display-name é uma cadeia de caracteres terminada em nulo que é preenchimento com um caractere nulo adicional, se necessário, para atingir um limite de 2 byte. O preenchimento no final da codificação **attFrom** consiste no número de caracteres nulos necessários para atingir um limite de **tamanho (TRP).** 
  
_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb 
    
Para o item **attFrom,** a estrutura **TRP** é sempre uma codificação única, portanto, o trpid fora do campo de estrutura **TRP** é **sempre trpidOneOff**. Os itens cbgrtrp, cch e cb correspondem aos campos restantes da **estrutura TRP.** 
  
O campo cbgrtrp é calculado como a soma de **(sizeof(TRP) \* 2),** o comprimento do sender-display-name terminada por nulo com seu preenchimento e o comprimento do endereço de remetente encerrado nulo.
  
O campo cch é calculado como o comprimento do nome de exibição terminada em nulo com seu preenchimento.
  
O campo cb é calculado como o comprimento do endereço de remetente encerrado nulo.
  
_sender-address:_ address-type **:** address **'\0'**
    
O endereço do remetente é uma cadeia de caracteres composta de quatro partes, o tipo de endereço, dois-pontos literais (:), o próprio endereço e um caractere nulo de terminação. Por exemplo, a cadeia `fax:1-909-555-1234\0` de caracteres seria um valor de endereço de remetente legal.
  

