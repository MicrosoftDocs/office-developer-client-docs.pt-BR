---
title: Nomeando pastas usando cadeias de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428309"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="6b77b-103">Nomeando pastas usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="6b77b-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="6b77b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b77b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b77b-105">Se você acessar uma ou mais pastas com frequência durante uma sessão, considere atribuir nomes às pastas com o método [IMsgStore::SetReceiveFolder.](imsgstore-setreceivefolder.md)</span><span class="sxs-lookup"><span data-stu-id="6b77b-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="6b77b-106">Embora **IMsgStore::SetReceiveFolder** seja usado principalmente para estabelecer pastas especiais para receber mensagens de entrada para determinadas classes de mensagens, ele também pode ser usado para associar qualquer pasta a um nome.</span><span class="sxs-lookup"><span data-stu-id="6b77b-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="6b77b-107">O nome pode ser igual à classe de mensagem ou pode ser qualquer cadeia de caracteres, personalizada para uso do cliente.</span><span class="sxs-lookup"><span data-stu-id="6b77b-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="6b77b-108">Associar um nome a uma pasta diminui o tempo necessário para encontrar e abrir a pasta.</span><span class="sxs-lookup"><span data-stu-id="6b77b-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

