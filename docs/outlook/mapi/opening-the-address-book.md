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
ms.openlocfilehash: 62a4e6a09570cc3d71b0797ed7fff162d05ee416
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583684"
---
# <a name="opening-the-address-book"></a>Abrir o catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chamar [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para abrir o catálogo de endereços integrada e recuperar um ponteiro para MAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) interface. Os métodos da interface **IAddrBook** podem ser usados para acessar as entradas em todos os contêineres de cada um dos provedores de catálogo de endereços no perfil. 
  
**OpenAddressBook** pode retornar um aviso, MAPI_W_ERRORS_RETURNED, para indicar que houve problemas com um ou mais dos provedores de catálogo de endereços. Clientes Interactive devem chamar [IMAPISession::GetLastError](imapisession-getlasterror.md) para recuperar informações de erro adicionais e exibir a hora de informações retornadas na primeira ligarem **OpenAddressBook** e retorna um aviso. 
  
Os clientes não-interativos devem ignore o aviso e prossiga como se o método foi bem-sucedido. A interface de **IAddrBook** retornada é válida independentemente se all, alguns ou nenhum dos provedores de catálogo de endereços no perfil estão sendo executados. Portanto, tanto interativos e clientes sempre devem se lembrar liberar o ponteiro **IAddrBook** quando a sessão será encerrada. 
  

