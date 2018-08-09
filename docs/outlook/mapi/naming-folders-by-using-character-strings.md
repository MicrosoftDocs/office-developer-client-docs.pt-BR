---
title: Nomear pastas usando cadeias de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768154"
---
# <a name="naming-folders-by-using-character-strings"></a>Nomear pastas usando cadeias de caracteres

  
  
**Aplica-se a**: Outlook 
  
Se você acessar pastas de um ou mais frequentemente durante uma sessão, considere atribuindo nomes às pastas com o método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Embora **IMsgStore::SetReceiveFolder** é usado principalmente para estabelecer pastas especiais para receber mensagens de entrada para as classes de mensagem específica, ele também pode ser usado para associar a um nome de qualquer pasta. O nome pode ser o mesmo que a classe de mensagem ou pode ser qualquer cadeia de caracteres, personalizada para uso do seu cliente. Associar um nome de uma pasta diminui o tempo que leva para localizar e abrir a pasta. 
  

