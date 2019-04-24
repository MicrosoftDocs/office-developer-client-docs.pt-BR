---
title: Nomear pastas usando cadeias de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326247"
---
# <a name="naming-folders-by-using-character-strings"></a>Nomear pastas usando cadeias de caracteres

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você acessar uma ou mais pastas com frequência durante uma sessão, considere a atribuição de nomes às pastas com o método [IMsgStore:: SetReceiveFolder](imsgstore-setreceivefolder.md) . Embora **IMsgStore:: SetReceiveFolder** seja usado principalmente para estabelecer pastas especiais para receber mensagens de entrada para classes de mensagens específicas, ele também pode ser usado para associar qualquer pasta com um nome. O nome pode ser o mesmo que a classe de mensagem ou pode ser qualquer cadeia de caracteres, personalizada para uso do cliente. A associação de um nome a uma pasta diminui o tempo necessário para localizar e abrir a pasta. 
  

