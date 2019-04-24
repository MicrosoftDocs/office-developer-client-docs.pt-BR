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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318113"
---
# <a name="attsentfor"></a>attSentFor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O atributo **attSentFor** é codificado como cadeias de caracteres contadas de ponta a ponta. O formato de **attSentFor** é o seguinte: 
  
 **attSentFor**: 
  
> display-name-Name de nome de exibição endereço de _email-endereço_
    
 _email-endereço_
  
> tipo **:** endereço 
    
Diferentemente de outros valores de comprimento, o nome de exibição e comprimento de endereço são valores de 16 bits não assinados em vez de inteiros longos não assinados. No entanto, eles ainda incluem o encerramento de caracteres nulos. As cadeias de caracteres de tipo e endereço na entrada de _endereço de email_ são separadas por um caractere de dois-pontos literal (:) caractere, como "SMTP:Joe@nowhere.com". Somente o tipo combinado **:** cadeia de caracteres de endereço é terminada em nulo.
  

