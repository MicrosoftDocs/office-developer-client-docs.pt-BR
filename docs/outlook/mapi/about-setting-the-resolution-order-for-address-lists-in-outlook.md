---
title: Sobre como definir a ordem de resolu��o de listas de endere�os no Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ltima altera��o: quinta-feira, 5 de julho de 2012'
ms.openlocfilehash: cfc640fd419ad030de6922fa61817881caa70d07
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766088"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="1425c-103">Sobre como definir a ordem de resolu��o de listas de endere�os no Outlook</span><span class="sxs-lookup"><span data-stu-id="1425c-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="1425c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1425c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1425c-105">Para cada perfil, Microsoft Office Outlook oferece suporte a várias listas de endereços e os usuários podem especificar manualmente a ordem das listas de endereços pelos quais destinatários em email participantes em solicitações de reunião e mensagens forem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="1425c-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="1425c-106">Por exemplo, voc� pode definir a ordem de resolu��o para que os nomes ser�o resolvidos primeiro contra seu cat�logo de endere�os do Outlook e, em seguida, a lista de endere�os Global.</span><span class="sxs-lookup"><span data-stu-id="1425c-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="1425c-107">Em um computador, um usu�rio pode abrir o cat�logo de endere�os, clique em **Ferramentas** e em seguida **Op��es** para especificar nesta ordem de resolu��o.</span><span class="sxs-lookup"><span data-stu-id="1425c-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="1425c-108">No entanto, em um ambiente corporativo, � mais eficiente para administradores de TI definir programaticamente a ordem das listas de endere�os pelo qual nomes forem resolvidos.</span><span class="sxs-lookup"><span data-stu-id="1425c-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="1425c-109">Esse tipo de c�digo pode ser usado como parte de um script de automa��o de inicializa��o que um administrador implanta dentro da corpora��o.</span><span class="sxs-lookup"><span data-stu-id="1425c-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="1425c-p102">MAPI oferece suporte ao m�todo **[SetSearchPath](iaddrbook-getsearchpath.md)** na interface do **[IAddrBook](iaddrbookimapiprop.md)**, que permite que voc� defina um novo caminho de pesquisa no perfil que ser� usado para resolu��o de nome. Para usar o m�todo **IAddrBook::SetSearchPath**, voc� deve especificar a ordem de resolu��o desejada usando uma matriz que cont�m os cont�ineres do endere�o relevante manuais online na ordem que eles devem ser resolvidos. Cada entrada nessa matriz tamb�m deve conter a identifica��o de entrada do cat�logo de endere�os correspondente.</span><span class="sxs-lookup"><span data-stu-id="1425c-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="1425c-113">A seguir est�o exemplos de c�digo de como especificar um caminho de pesquisa personalizada para listas de endere�os.</span><span class="sxs-lookup"><span data-stu-id="1425c-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="1425c-114">Definir a ordem de resolução de listas de endereços de forma programática</span><span class="sxs-lookup"><span data-stu-id="1425c-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="1425c-115">KB 292590: como alterar a ordem de classifica��o do cat�logo de endere�os com SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="1425c-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](http://support.microsoft.com/kb/292590)
    

