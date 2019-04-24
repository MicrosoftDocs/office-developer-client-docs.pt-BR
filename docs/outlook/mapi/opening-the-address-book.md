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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326163"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="2c206-103">Abrir o catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="2c206-103">Opening the address book</span></span>

<span data-ttu-id="2c206-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c206-105">Chame [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) para abrir o catálogo de endereços integrado e recuperar um ponteiro para a interface MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="2c206-105">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface.</span></span> <span data-ttu-id="2c206-106">Os métodos da interface **IAddrBook** podem ser usados para acessar entradas em todos os contêineres de cada um dos provedores de catálogo de endereços no perfil.</span><span class="sxs-lookup"><span data-stu-id="2c206-106">The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="2c206-107">**OpenAddressBook** pode retornar um aviso, MAPI_W_ERRORS_RETURNED, para indicar que houve problemas com um ou mais dos provedores de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="2c206-107">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers.</span></span> <span data-ttu-id="2c206-108">Os clientes interAtivos devem chamar [IMAPISession:: GetLastError](imapisession-getlasterror.md) para recuperar informações de erro adicionais e exibir as informações retornadas na primeira vez que chamarem **OpenAddressBook** e retornará um aviso.</span><span class="sxs-lookup"><span data-stu-id="2c206-108">Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="2c206-109">Os clientes não interativos devem ignorar o aviso e prosseguir como se o método fosse bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2c206-109">Noninteractive clients should ignore the warning and proceed as if the method succeeded.</span></span> <span data-ttu-id="2c206-110">A interface **IAddrBook** retornada é válida independentemente de todos, alguns ou nenhum dos provedores de catálogo de endereços no perfil estão em execução.</span><span class="sxs-lookup"><span data-stu-id="2c206-110">The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running.</span></span> <span data-ttu-id="2c206-111">Portanto, os clientes interativos e não interativos devem sempre se lembrar de liberar o ponteiro do **IAddrBook** quando a sessão terminar.</span><span class="sxs-lookup"><span data-stu-id="2c206-111">Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

