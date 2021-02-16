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
# <a name="opening-the-address-book"></a>Abrir o catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chame [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) para abrir o livro de endereços integrado e recuperar um ponteiro para a interface [IAddrBook de MAPI: IMAPIProp.](iaddrbookimapiprop.md) Os métodos da interface **IAddrBook** podem ser usados para acessar entradas em todos os contêineres de cada um dos provedores de livro de endereços no perfil. 
  
**OpenAddressBook** pode retornar um aviso, MAPI_W_ERRORS_RETURNED, para indicar que houve problemas com um ou mais provedores de agendas. Os clientes interativos devem chamar [IMAPISession::GetLastError](imapisession-getlasterror.md) para recuperar informações de erro adicionais e exibir as informações retornadas na primeira vez que chamarem **OpenAddressBook** e retornar um aviso. 
  
Os clientes não-inativos devem ignorar o aviso e prosseguir como se o método tivesse sido bem-sucedido. A interface **IAddrBook** retornada é válida independentemente de todos, alguns ou nenhum dos provedores de livro de endereços no perfil estão em execução. Portanto, os clientes interativos e não interativos devem sempre se lembrar de liberar o ponteiro **IAddrBook** quando a sessão terminar. 
  

