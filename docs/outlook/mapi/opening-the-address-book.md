---
title: Abrir o catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4b9d7b8cf71b4e00dac6022e1dda727ef7a23036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768176"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="b10c5-103">Abrir o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="b10c5-103">Opening the address book</span></span>

<span data-ttu-id="b10c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b10c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b10c5-105">Chamar [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para abrir o catálogo de endereços integrada e recuperar um ponteiro para MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface.</span><span class="sxs-lookup"><span data-stu-id="b10c5-105">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface.</span></span> <span data-ttu-id="b10c5-106">Os métodos da interface **IAddrBook** podem ser usados para acessar as entradas em todos os contêineres de cada um dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="b10c5-106">The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="b10c5-107">**OpenAddressBook** pode retornar um aviso, MAPI_W_ERRORS_RETURNED, para indicar que houve problemas com um ou mais dos provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="b10c5-107">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers.</span></span> <span data-ttu-id="b10c5-108">Clientes Interactive devem chamar [IMAPISession::GetLastError](imapisession-getlasterror.md) para recuperar informações de erro adicionais e exibir a hora de informações retornadas na primeira ligarem **OpenAddressBook** e retorna um aviso.</span><span class="sxs-lookup"><span data-stu-id="b10c5-108">Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="b10c5-109">Os clientes não-interativos devem ignore o aviso e prossiga como se o método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b10c5-109">Noninteractive clients should ignore the warning and proceed as if the method succeeded.</span></span> <span data-ttu-id="b10c5-110">A interface de **IAddrBook** retornada é válida independentemente se all, alguns ou nenhum dos provedores de catálogo de endereços no perfil estão sendo executados.</span><span class="sxs-lookup"><span data-stu-id="b10c5-110">The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running.</span></span> <span data-ttu-id="b10c5-111">Portanto, tanto interativos e clientes sempre devem se lembrar liberar o ponteiro **IAddrBook** quando a sessão será encerrada.</span><span class="sxs-lookup"><span data-stu-id="b10c5-111">Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

