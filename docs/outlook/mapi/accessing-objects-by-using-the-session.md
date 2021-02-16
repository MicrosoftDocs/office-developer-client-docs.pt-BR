---
title: Acessando objetos usando a sessão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410536"
---
# <a name="accessing-objects-by-using-the-session"></a>Acessando objetos usando a sessão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O ponteiro de sessão que você recebe de sua chamada para [MAPILogonEx](mapilogonex.md) pode ser usado para acessar uma ampla variedade de objetos. A tabela a seguir lista os métodos usados para acessar vários objetos: 
  
|**Object**|**Método Session**|
|:-----|:-----|
|Seção Profile  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Armazenamento de mensagens  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Catálogo de endereços  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administração do serviço de mensagens  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Pasta, mensagem, contêiner do livro de endereços, lista de distribuição ou usuário de mensagens  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Com o **método OpenEntry** e um identificador de entrada válido, você pode abrir qualquer objeto de provedor de armazenamento de mensagens ou de um livro de endereços. Há outros **métodos OpenEntry** em MAPI, além do **método IMAPISession.** **OpenEntry** é implementado nos seguintes objetos: 
  
|**Object**|**Method**|
|:-----|:-----|
|Objeto de logon do provedor de agendas  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Catálogo de endereços  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contêiner do livro de endereços  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sessão  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Armazenamento de mensagens  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de logon do provedor de armazenamento de mensagens  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto Support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Alguns **métodos OpenEntry** exigem que um identificador de entrada do objeto seja aberto, assim como **IMAPISession::OpenEntry**; outros métodos permitem que NULL seja especificado. Um identificador de entrada NULL é interpretado de forma diferente, dependendo do objeto. Por exemplo, quando você chama **IAddrBook::OpenEntry** com um identificador de entrada NULL, MAPI abre o contêiner raiz do livro de endereços. O método **OpenEntry** do armazenamento de mensagens se comporta da mesma forma; ele abre a pasta raiz do armazenamento de mensagens. **IMAPIContainer::OpenEntry**, implementado por pastas e contêineres de livro de endereços, pode retornar MAPI_E_INVALID_PARAMETER contêiner raiz, dependendo do implementador. 
  
Além de não permitir um valor NULL para o identificador de entrada, o método **OpenEntry** da sessão difere de outros métodos **OpenEntry** porque seu trabalho não é abrir objetos. Em vez disso, ele examina o identificador de entrada e encaminha a chamada para **outro método OpenEntry** implementado pelo provedor de serviços apropriado. Por exemplo, se você chamar **IMAPISession::OpenEntry** com o identificador de entrada de uma mensagem, o MAPI chamará o método **IMSLogon::OpenEntry** do armazenamento de mensagens responsável pela mensagem. 
  
Além de usar a sessão para abrir objetos, os clientes a usam para compará-los. O [método IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compara objetos comparando seus identificadores de entrada. Se as [estruturas MAPIUID](mapiuid.md) contidas nos identificadores de entrada pertencerem ao mesmo provedor de serviços, o MAPI encaminhará a chamada para esse provedor. **CompareEntryIDs** retorna um valor de erro quando os dois identificadores de entrada não são comparados. Embora esse método possa comparar identificadores de entrada que pertencem a qualquer tipo de objeto, **CompareEntryIDs** funciona melhor para objetos de nível superior, como armazenamentos de mensagens e contêineres de address book. Para comparar objetos de nível inferior, compare diretamente as teclas de pesquisa dos objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou as teclas de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Assim **como OpenEntry**, **CompareEntryIDs** é implementado por vários objetos. Escolha qual **método OpenEntry** e **CompareEntryID** usar de acordo com a quantidade de informações que você tem sobre o objeto ou objetos a serem abertos ou comparados. Use as diretrizes a seguir ao decidir qual método de interface chamar: 
  
- Se você não tiver informações sobre os objetos de destino, chame [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Essa abordagem permite o acesso a qualquer objeto, mas é a mais lenta dos três.
    
- Se você sabe que os objetos de destino são entradas do livro de endereços em vez de, por exemplo, pastas, chame o método [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md) **IAddrBook::OpenEntry** abre o contêiner raiz do livro de endereços quando NULL é especificado como o objeto de destino. Essa abordagem permite o acesso a qualquer objeto de livro de endereços e é mais rápida do que usar **IMAPISession**, mas mais lento do que usar **IMAPIContainer**.
    
- Se o identificador de entrada que está sendo usado for um identificador de entrada de curto prazo ou se você sabe que os objetos de destino pertencem a um determinado contêiner ou pasta do livro de endereços, chame o método [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Essa abordagem produz o desempenho mais rápido, mas permite o acesso apenas a objetos em um contêiner ou pasta específica. 
    

