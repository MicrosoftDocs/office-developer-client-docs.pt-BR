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
ms.openlocfilehash: f0696ad4d15274e4af18d2246dd124c1bfee1a2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589403"
---
# <a name="accessing-objects-by-using-the-session"></a>Acessar objetos usando a sessão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O ponteiro de sessão que você recebe de sua chamada à [MAPILogonEx](mapilogonex.md) pode ser usado para acessar uma ampla variedade de objetos. A tabela a seguir lista os métodos que são usados para acessar vários objetos: 
  
|**Object**|**Método de sessão**|
|:-----|:-----|
|Seção de perfil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Armazenamento de mensagens  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Catálogo de endereços  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administração do serviço de mensagem  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Pasta, mensagem, o contêiner de catálogo de endereços, lista de distribuição ou usuário de mensagens  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Com o método **OpenEntry** e um identificador de entrada válida, você pode abrir o objeto de provedor do repositório qualquer endereço catálogo ou mensagem. Há outros métodos **OpenEntry** no MAPI, além do método **IMAPISession** . **OpenEntry** é implementada nos seguintes objetos: 
  
|**Object**|**Method**|
|:-----|:-----|
|Objeto de logon do provedor do catálogo de endereços  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Catálogo de endereços  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contêiner de catálogo de endereços  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sessão  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Armazenamento de mensagens  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de logon do provedor de repositório de mensagem  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto de suporte  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Alguns métodos **OpenEntry** exigem um identificador de entrada do objeto a ser aberto, como o **IMAPISession::OpenEntry**; outros métodos permitem NULL deve ser especificado. Um identificador de entrada NULL será interpretado forma diferente, dependendo do objeto. Por exemplo, quando você chama **IAddrBook::OpenEntry** com um identificador de entrada NULL, MAPI abre o contêiner de raiz do catálogo de endereços. Método de **OpenEntry** da loja mensagem se comporta da mesma forma; ele abre a pasta raiz do armazenamento de mensagens. **IMAPIContainer::OpenEntry**, implementada por pastas e contêineres do catálogo de endereços, deverá retornar MAPI_E_INVALID_PARAMETER ou no contêiner de raiz, dependendo do implementador. 
  
Além das proibindo um valor NULL para o identificador de entrada, **OpenEntry** método da sessão difere outros métodos **OpenEntry** porque seu trabalho não é abrir objetos. Em vez disso, ele examina o identificador de entrada e encaminha a chamada para outro método **OpenEntry** implementada pelo provedor de serviço apropriado. Por exemplo, se você chamar **IMAPISession::OpenEntry** com o identificador de entrada de uma mensagem, MAPI chama o método **IMSLogon::OpenEntry** o armazenamento de mensagens responsável pela mensagem. 
  
Além de usar a sessão para abrir objetos, clientes usá-lo para compará-los. O método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compara objetos comparando seus identificadores de entrada. Se as estruturas [MAPIUID](mapiuid.md) contidas os identificadores de entrada pertencem ao mesmo provedor de serviços, MAPI encaminha a chamada para esse provedor. **CompareEntryIDs** retorna um valor de erro quando os identificadores de duas entrada não coincidem. Embora esse método pode comparar identificadores de entrada que pertencem a qualquer tipo de objeto, **CompareEntryIDs** funciona melhor para objetos de nível superior, como repositórios de mensagem e contêineres do catálogo de endereços. Para comparar os objetos de nível inferior, compare diretamente chaves de pesquisa dos objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou chaves de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Como **OpenEntry**, **CompareEntryIDs** é implementado por vários objetos. Escolha qual método **OpenEntry** e **CompareEntryID** usar acordo com a quantidade de informações que você precisa sobre um ou mais objetos deve ser aberto ou comparados. Use as seguintes diretrizes ao decidir qual método de interface de chamada: 
  
- Se você não tiver nenhuma informação sobre os objetos de destino, chame [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Essa abordagem permite o acesso a qualquer objeto, mas é o mais lento dos três.
    
- Se você souber que os objetos de destino são entradas do catálogo de endereços em vez de, por exemplo, pastas, chame o método [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook::OpenEntry** abre o contêiner de raiz do catálogo de endereços quando NULL é especificado como o objeto de destino. Essa abordagem permite o acesso a qualquer objeto de catálogo de endereços e é mais rápido que usar **IMAPISession**, mas mais lenta do que usando **IMAPIContainer**.
    
- Se o identificador de entrada que está sendo usado é um identificador de entrada de curto prazo ou se você souber que os objetos de destino pertencem a uma pasta ou um contêiner de catálogo de endereço específica, chame o método de [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) . Essa abordagem produz o desempenho mais rápido, mas permite o acesso somente aos objetos em um contêiner específico ou pasta. 
    

