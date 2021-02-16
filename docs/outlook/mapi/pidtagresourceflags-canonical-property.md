---
title: Propriedade canônica PidTagResourceFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceFlags
api_type:
- COM
ms.assetid: 69be9ad3-006a-459e-9cd4-eb3f609d71ad
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2fb9eed0beaf7269ac90a021dae650355484ebc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436227"
---
# <a name="pidtagresourceflags-canonical-property"></a>Propriedade canônica PidTagResourceFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores para provedores e serviços de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_FLAGS  <br/> |
|Identificador:  <br/> |0x3009  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade descreve as características de um serviço de mensagem, um provedor de serviços ou um objeto de status. Os sinalizadores definidos para essa propriedade dependem de seu contexto. Por exemplo, alguns sinalizadores são válidos apenas para objetos de status e outros sinalizadores somente para colunas na tabela de serviço de mensagens. 
  
Os sinalizadores são de três classes: estática, modificável e dinâmica. Sinalizadores estáticos são definidos por MAPI a partir de dados em MAPISVC. INF e nunca alterado. Sinalizadores modificáveis são definidos por MAPI de MAPISVC. INF, mas pode ser alterado posteriormente. Sinalizadores dinâmicos podem ser definidos e redefinidos por métodos MAPI.
  
Para um serviço de mensagens, um ou mais dos seguintes sinalizadores podem ser definidos nesta propriedade:
  
SERVICE_CREATE_WITH_STORE 
  
> Reservado. Não usar.
    
SERVICE_DEFAULT_STORE 
  
> Dinâmico. O serviço de mensagens contém o armazenamento padrão. Uma interface do usuário deve ser exibida solicitando que o usuário confirme antes de excluir ou mover esse serviço para fora do perfil. 
    
SERVICE_NO_PRIMARY_IDENTITY 
  
> Estático. O sinalizador de nível de serviço que deve ser definido para indicar que nenhum dos provedores no serviço de mensagens pode ser usado para fornecer uma identidade. Esse sinalizador ou SERVICE_PRIMARY_IDENTITY deve ser definido, mas não ambos.
    
SERVICE_PRIMARY_IDENTITY 
  
> Modificável. O serviço de mensagens correspondente contém o provedor usado para a identidade principal desta sessão. Use [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) para definir esse sinalizador. Esse sinalizador ou SERVICE_NO_PRIMARY_IDENTITY devem ser definidos, mas não ambos. 
    
SERVICE_SINGLE_COPY 
  
> Estático. Qualquer tentativa de criar ou copiar esse serviço de mensagem em um perfil onde o serviço já existe falhará. Para criar um serviço de mensagem de cópia **única, PR_RESOURCE_FLAGS** a propriedade PR_RESOURCE_FLAGS seção do serviço no MAPISVC. INF e de definir esse sinalizador. 
    
Para um provedor de serviços, um ou mais dos seguintes sinalizadores podem ser definidos **PR_RESOURCE_FLAGS:**
  
HOOK_INBOUND 
  
> Estático. O gancho do spooler precisa processar mensagens de entrada.
    
HOOK_OUTBOUND 
  
> Estático. O gancho do spooler precisa processar mensagens de saída. 
    
STATUS_DEFAULT_OUTBOUND 
  
> Modificável. Essa identidade deve ser aplicada a mensagens de saída se o perfil contiver várias instâncias deste provedor de transporte. Isso pode acontecer se várias instâncias de um único provedor de transporte aparecerem no perfil.
    
STATUS_DEFAULT_STORE 
  
> Modificável. Esse armazenamento de mensagens é o armazenamento padrão do perfil. 
    
STATUS_NEED_IPM_TREE 
  
> Dinâmico. As pastas padrão nesse armazenamento de mensagens, incluindo a pasta raiz da mensagem interpersonal (IPM), ainda não foram verificadas. MAPI define e limpa esse sinalizador. 
    
STATUS_NO_DEFAULT_STORE 
  
> Estático. Esse armazenamento de mensagens não consegue se tornar o armazenamento de mensagens padrão para o perfil.
    
STATUS_NO_PRIMARY_IDENTITY 
  
> Estático. Esse provedor não fornece uma identidade em sua linha de status. Esse sinalizador ou STATUS_PRIMARY_IDENTITY deve ser definido.
    
STATUS_OWN_STORE 
  
> Estático. Esse provedor de transporte está fortemente unido a um repositório de mensagens e fornece a PR_OWN_STORE_ENTRYID **(** [PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) em sua linha de status.
    
STATUS_PRIMARY_IDENTITY 
  
> Modificável. Esse provedor fornece a identidade principal da sessão; o identificador de entrada do objeto que fornece a identidade é retornado de [IMAPISession::QueryIdentity](imapisession-queryidentity.md). Esse sinalizador ou **STATUS_NO_PRIMARY_IDENTITY** deve ser definido. 
    
STATUS_PRIMARY_STORE 
  
> Modificável. Esse armazenamento de mensagens deve ser usado quando um aplicativo cliente faz o login. Depois de aberto, esse armazenamento deve ser definido como o armazenamento padrão para o perfil. 
    
STATUS_SECONDARY_STORE 
  
> Modificável. Esse armazenamento de mensagens deve ser usado se o armazenamento principal não estiver disponível quando um aplicativo cliente faz o login. Depois de aberto, esse armazenamento deve ser definido como o armazenamento padrão para o perfil. 
    
STATUS_SIMPLE_STORE 
  
> Dinâmico. Esse armazenamento de mensagens será usado pelo Simple MAPI como seu armazenamento de mensagens padrão.
    
STATUS_TEMP_SECTION 
  
> Dinâmico. Esse armazenamento de mensagens não deve ser publicado na tabela do armazenamento de mensagens e será excluído do perfil após o logoff. 
    
STATUS_XP_PREFER_LAST 
  
> Estático. Esse transporte espera ser o último transporte selecionado para enviar uma mensagem quando vários provedores de transporte são capazes de transmitir a mensagem.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md)
  
[Propriedade canônica PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

