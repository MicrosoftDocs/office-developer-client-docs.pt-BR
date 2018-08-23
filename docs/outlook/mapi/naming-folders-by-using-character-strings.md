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
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594583"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="bb520-103">Nomear pastas usando cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="bb520-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="bb520-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb520-105">Se você acessar pastas de um ou mais frequentemente durante uma sessão, considere atribuindo nomes às pastas com o método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="bb520-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="bb520-106">Embora **IMsgStore::SetReceiveFolder** é usado principalmente para estabelecer pastas especiais para receber mensagens de entrada para as classes de mensagem específica, ele também pode ser usado para associar a um nome de qualquer pasta.</span><span class="sxs-lookup"><span data-stu-id="bb520-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="bb520-107">O nome pode ser o mesmo que a classe de mensagem ou pode ser qualquer cadeia de caracteres, personalizada para uso do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="bb520-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="bb520-108">Associar um nome de uma pasta diminui o tempo que leva para localizar e abrir a pasta.</span><span class="sxs-lookup"><span data-stu-id="bb520-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

