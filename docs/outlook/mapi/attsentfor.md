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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408835"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O **atributo attSentFor** é codificado como cadeias de caracteres contadas colocadas de ponta a ponta. O formato **para attSentFor** é o seguinte: 
  
 **attSentFor**: 
  
> display-name-length display-name address-length  _email-address_
    
 _email-address_
  
> tipo **:** endereço 
    
Ao contrário de outros valores de comprimento, o tamanho do nome de exibição e o comprimento do endereço são valores de 16 bits não assinados em vez de inteiros longos não assinados. No entanto, eles ainda incluem a terminação de caracteres nulos. As cadeias de caracteres de tipo e endereço na entrada  _de endereço_ de email são separadas por dois-pontos literais (:) caractere, como "smtp:joe@nowhere.com". Somente o tipo combinado **: cadeia** de caracteres de endereço é terminada em nulo.
  

