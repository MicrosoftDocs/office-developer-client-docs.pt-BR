---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427651"
---
# <a name="attowner"></a>attOwner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O **atributo attOwner** é codificado como cadeias de caracteres contadas colocadas de ponta a ponta. O formato para **attOwner** é o seguinte: 
  
 **attOwner**: 
  
> display-name-length display-name address-length  _email-address_
    
 _email-address_
  
> tipo **:** endereço 
    
Ao contrário de outros valores de comprimento, o tamanho do nome de exibição e o comprimento do endereço são valores de 16 bits não assinados em vez de inteiros longos não assinados. No entanto, eles ainda incluem a terminação de caracteres nulos. As cadeias de caracteres de tipo e endereço na entrada  _de endereço_ de email são separadas por dois-pontos literais (:) caractere, como "smtp:joe@nowhere.com". Somente o tipo **combinado: cadeia** de caracteres de endereço é terminada em nulo.
  
O mapeamento das propriedades MAPI para o **atributo attOwner** depende da classe de mensagem da mensagem que está sendo codificada. 
  

