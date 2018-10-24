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
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594583"
---
# <a name="naming-folders-by-using-character-strings"></a>Nomear pastas usando cadeias de caracteres

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se você acessar pastas de um ou mais frequentemente durante uma sessão, considere atribuindo nomes às pastas com o método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) . Embora **IMsgStore::SetReceiveFolder** é usado principalmente para estabelecer pastas especiais para receber mensagens de entrada para as classes de mensagem específica, ele também pode ser usado para associar a um nome de qualquer pasta. O nome pode ser o mesmo que a classe de mensagem ou pode ser qualquer cadeia de caracteres, personalizada para uso do seu cliente. Associar um nome de uma pasta diminui o tempo que leva para localizar e abrir a pasta. 
  

