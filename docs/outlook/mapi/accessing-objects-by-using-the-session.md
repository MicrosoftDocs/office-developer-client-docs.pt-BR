---
title: Acessar objetos usando a sessão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321704"
---
# <a name="accessing-objects-by-using-the-session"></a>Acessar objetos usando a sessão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O ponteiro de sessão recebido de sua chamada para [funçãomapilogonex](mapilogonex.md) pode ser usado para acessar uma ampla variedade de objetos. A tabela a seguir lista os métodos que são usados para acessar vários objetos: 
  
|**Object**|**Método de sessão**|
|:-----|:-----|
|Seção Profile  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Repositório de mensagens  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Catálogo de endereços  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administração do serviço de mensagens  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Pasta, mensagem, contêiner de catálogo de endereços, lista de distribuição ou usuário de mensagens  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Com o método **OpenEntry** e um identificador de entrada válido, você pode abrir qualquer catálogo de endereços ou objeto de provedor de repositório de mensagens. Há outros métodos **OpenEntry** em MAPI, além do método **IMAPISession** . **OpenEntry** é implementado nos seguintes objetos: 
  
|**Object**|**Method**|
|:-----|:-----|
|Objeto de logon do provedor de catálogo de endereços  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Catálogo de endereços  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contêiner de catálogo de endereços  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sessão  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Repositório de mensagens  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de logon do provedor de repositório de mensagens  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Pasta  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Alguns métodos **OpenEntry** exigem um identificador de entrada do objeto a ser aberto, como o **IMAPISession:: OpenEntry**; outros métodos permitem que NULL seja especificado. Um identificador de entrada nulo é interpretado de forma diferente dependendo do objeto. Por exemplo, quando você chama **IAddrBook:: OpenEntry** com um identificador de entrada nulo, MAPI abre o contêiner raiz do catálogo de endereços. O método **OpenEntry** do armazenamento de mensagens se comporta de forma semelhante; Ele abre a pasta raiz do repositório de mensagens. **IMAPIContainer:: OpenEntry**, implementado por contêineres de pastas e catálogos de endereços, pode retornar MAPI_E_INVALID_PARAMETER ou o contêiner raiz, dependendo do implementador. 
  
Além de não permitir um valor nulo para o identificador de entrada, o método **OpenEntry** da sessão difere de outros métodos **OpenEntry** porque seu trabalho não é abrir objetos. Em vez disso, ele examina o identificador de entrada e encaminha a chamada para outro método **OpenEntry** implementado pelo provedor de serviços apropriado. Por exemplo, se você chamar **IMAPISession:: OpenEntry** com o identificador de entrada de uma mensagem, MAPI chamará o método **IMSLogon:: OpenEntry** do repositório de mensagens responsável pela mensagem. 
  
Além de usar a sessão para abrir objetos, os clientes o utilizam para compará-los. O método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) compara objetos comparando seus identificadores de entrada. Se as estruturas [MAPIUID](mapiuid.md) contidas nos identificadores de entrada pertencerem ao mesmo provedor de serviços, o MAPI encaminha a chamada para esse provedor. **CompareEntryIDs** retorna um valor de erro quando os dois identificadores de entrada não coincidem. Embora esse método possa comparar identificadores de entrada que pertencem a qualquer tipo de objeto, **CompareEntryIDs** funciona melhor para objetos de nível superior, como repositórios de mensagens e contêineres de catálogo de endereços. Para comparar objetos de nível inferior, Compare diretamente as chaves de pesquisa dos objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou as chaves de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Como o **OpenEntry**, o **CompareEntryIDs** é implementado por vários objetos. Escolha o método **OpenEntry** e **CompareEntryID** a ser usado de acordo com a quantidade de informações que você tem sobre o objeto ou objetos a serem abertos ou comparados. Use as diretrizes a seguir ao decidir que método de interface chamar: 
  
- Se você não tiver informações sobre os objetos de destino, chame [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md). Essa abordagem permite o acesso a qualquer objeto, mas é a mais lenta dos três.
    
- Se você souber que os objetos de destino são entradas do catálogo de endereços, em vez de, por exemplo, pastas, chame o método [IAddrBook:: OpenEntry](iaddrbook-openentry.md) ou [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook:: OpenEntry** abre o contêiner raiz do catálogo de endereços quando NULL é especificado como o objeto de destino. Essa abordagem permite o acesso a qualquer objeto do catálogo de endereços e é mais rápida do que o uso do **IMAPISession**, mas mais lenta do que o uso do **IMAPIContainer**.
    
- Se o identificador de entrada que está sendo usado for um identificador de entrada de curto prazo ou se você souber que os objetos de destino pertencem a um determinado contêiner ou pasta de catálogo de endereços, chame o método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) . Essa abordagem produz o desempenho mais rápido, mas permite o acesso somente a objetos em um contêiner ou pasta específica. 
    

