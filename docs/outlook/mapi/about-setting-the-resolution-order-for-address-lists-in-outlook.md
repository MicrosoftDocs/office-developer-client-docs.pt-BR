---
title: Sobre como definir a ordem de resolução de listas de endereços no Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Última modificação: 05 de julho de 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321830"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a><span data-ttu-id="abf49-103">Sobre como definir a ordem de resolução de listas de endereços no Outlook</span><span class="sxs-lookup"><span data-stu-id="abf49-103">About Setting the Resolution Order for Address Lists in Outlook</span></span>

  
  
<span data-ttu-id="abf49-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="abf49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="abf49-105">Para cada perfil, o Microsoft Office Outlook suporta várias listas de endereços e os usuários podem especificar manualmente a ordem das lista de endereços pelas quais são resolvidos os recebedores de mensagens de email e os participantes de solicitações de reunião.</span><span class="sxs-lookup"><span data-stu-id="abf49-105">For each profile, Microsoft Office Outlook supports multiple address lists and users can manually specify the order of address lists by which recipients in email messages and attendees in meeting requests are resolved.</span></span> <span data-ttu-id="abf49-106">Por exemplo, você pode definir a ordem de resolução para que os nomes sejam resolvidos primeiro de acordo com seu Catálogo de Endereços do Outlook, e depois de acordo com a Lista de Endereços Global.</span><span class="sxs-lookup"><span data-stu-id="abf49-106">For example, you can set the resolution order so that names are resolved first against your Outlook Address Book, and then against the Global Address List.</span></span> <span data-ttu-id="abf49-107">Em um computador, um usuário pode abrir o catálogo de endereços, clicar em **Ferramentas** e, em seguida, em **Opções** para especificar esta ordem de resolução.</span><span class="sxs-lookup"><span data-stu-id="abf49-107">On a computer, a user can open the Address Book, click **Tools** and then **Options** to specify this resolution order.</span></span> <span data-ttu-id="abf49-108">No entanto, em um ambiente corporativo, é mais eficiente para os administradores de TI definir programaticamente a ordem das listas de endereços segundo a qual os nomes são resolvidos.</span><span class="sxs-lookup"><span data-stu-id="abf49-108">However, in a corporate environment, it is more efficient for IT administrators to programmatically set the order of address lists by which names are resolved.</span></span> <span data-ttu-id="abf49-109">Este código pode ser usado como parte de um script de automação de inicialização que um administrador implanta dentro da corporação.</span><span class="sxs-lookup"><span data-stu-id="abf49-109">Such code can be used as part of a startup automation script that an administrator deploys inside the corporation.</span></span> 
  
<span data-ttu-id="abf49-p102">A MAPI suporta o método **[SetSearchPath](iaddrbook-getsearchpath.md)** na interface **[IAddrBook](iaddrbookimapiprop.md)**, o que permite que você defina um novo caminho de pesquisa no perfil usado para a resolução dos nomes. Para usar o método **IAddrBook::SetSearchPath**, você precisa especificar a ordem de resolução desejada usando uma matriz com contêineres dos catálogos de endereços relevantes na ordem em que eles devem ser resolvidos. Cada entrada nessa matriz também deve conter a ID de entrada do catálogo de endereços correspondente.</span><span class="sxs-lookup"><span data-stu-id="abf49-p102">MAPI supports the **[SetSearchPath](iaddrbook-getsearchpath.md)** method in the **[IAddrBook](iaddrbookimapiprop.md)** interface, which allows you to set a new search path in the profile that is used for name resolution. To use the **IAddrBook::SetSearchPath** method, you must specify the desired resolution order by using an array that holds containers of the relevant address books in the order they should be resolved. Each entry in that array should also contain the entry ID of the corresponding address book.</span></span> 
  
<span data-ttu-id="abf49-113">A seguir estão exemplos de código de como especificar um caminho de pesquisa personalizado para catálogos de endereços.</span><span class="sxs-lookup"><span data-stu-id="abf49-113">The following are code examples of how to specify a custom search path for address lists.</span></span>
  
- [<span data-ttu-id="abf49-114">Definir programaticamente a ordem de resolução para catálogos de endereços</span><span class="sxs-lookup"><span data-stu-id="abf49-114">Programmatically Set the Resolution Order for Address Lists</span></span>](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [<span data-ttu-id="abf49-115">KB 292590: Como alterar a ordem de classificação do catálogo de endereços com SetSearchPath</span><span class="sxs-lookup"><span data-stu-id="abf49-115">KB 292590: How To Change Address Book Sort Order with SetSearchPath</span></span>](https://support.microsoft.com/kb/292590)
    

