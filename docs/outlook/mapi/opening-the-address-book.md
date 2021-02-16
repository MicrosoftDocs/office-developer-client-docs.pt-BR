---
title: Abrir o catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404544"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="d9bb6-103">Abrir o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="d9bb6-103">Opening the address book</span></span>

<span data-ttu-id="d9bb6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9bb6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9bb6-105">Chame [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para abrir o livro de endereços integrado e recuperar um ponteiro para a interface [IAddrBook de MAPI: IMAPIProp.](iaddrbookimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="d9bb6-105">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface.</span></span> <span data-ttu-id="d9bb6-106">Os métodos da interface **IAddrBook** podem ser usados para acessar entradas em todos os contêineres de cada um dos provedores de livro de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-106">The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="d9bb6-107">**OpenAddressBook** pode retornar um aviso, MAPI_W_ERRORS_RETURNED, para indicar que houve problemas com um ou mais provedores de agendas.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-107">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers.</span></span> <span data-ttu-id="d9bb6-108">Os clientes interativos devem chamar [IMAPISession::GetLastError](imapisession-getlasterror.md) para recuperar informações de erro adicionais e exibir as informações retornadas na primeira vez que chamarem **OpenAddressBook** e retornar um aviso.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-108">Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="d9bb6-109">Os clientes não-inativos devem ignorar o aviso e prosseguir como se o método tivesse sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-109">Noninteractive clients should ignore the warning and proceed as if the method succeeded.</span></span> <span data-ttu-id="d9bb6-110">A interface **IAddrBook** retornada é válida independentemente de todos, alguns ou nenhum dos provedores de livro de endereços no perfil estão em execução.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-110">The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running.</span></span> <span data-ttu-id="d9bb6-111">Portanto, os clientes interativos e não interativos devem sempre se lembrar de liberar o ponteiro **IAddrBook** quando a sessão terminar.</span><span class="sxs-lookup"><span data-stu-id="d9bb6-111">Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

